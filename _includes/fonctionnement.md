Le fichier gift obtenu contient un code html qui appelle un script que l'on appellera "Script intégrateur".
Ce script intégrateur intègre la page web de l'exerciseur directement dans la page moodle (via ce qu'on apelle une iframe), la page web ne reçoit aucune information personnelle (en dehors des données techniques envoyés lorsque l'on visite n'importe quelle page web comme l'adresse ip).
La page web de l'exerciseur communique ensuite le résultat de l'exercice au script intégrateur qui se charge ensuite de communiquer la note à moodle.

<!--
https://mermaid.live/edit#pako:eNp1U7uO2zAQ_JUFU7hxkF4IDASJOyuNWzdramgToEgeH8IdDvcvKXP5Df1YSEmxdblEhURxZ3dmZ8lnIV0H0YiIhwwr8U3zJXB_slQezsnZ3J8R5n_PIWmpPdtELXGk1rnO4H3wOActRRm0T-8B-wo4bPCIIHVEXgg-fHcJ5AYEardHaujAVHTFpEut8qFscd_oQOnJlxceU93WRTAZjfz5HOjTroSlswlWB-ryguIB8m2VitGwtfYbuS193O2oiviilJZXkFmJqWzyyuEC6m99zrxIZBBJW-UixRzILH1K0PhjyVoaPk4kbSH5yhMFarz3sTYXxlfvbERdr7n7yXVaV9jXCrMcs8nBTCl32o5tnLrWqgx3Gdja65p_2IyvZvw5gKAUZMrrEnPK_ubJenYU0Fejq_ooXZjaNDy7oWDHX6nslfGjggbNpS57Td7F1CJGvuBvN-5np_phL5MBA5vK1i3z_YdR03RvKty5DD__52SJregRetZdOf3PFXQS6YpijmjKsoPibNJJnOxLgdabcHyyUjQpZGxF9h2nP5dFNIpNxMtv-WUgdQ
-->
<!--
sequenceDiagram
    autonumber
    participant M as Moodle
    participant S as Mon script
    participant E as L'exerciseur
    #Note over M,S : La question est une question de type texte qui au lieu<br />de contenir du texte avec une question contient un script
    M ->> S : Affiche la question qui charge mon script<br />et les infos sur l'exercice à charger
    S ->> M : Cache le champs de réponse de la question moodle 
    S ->> E : Charge l'url de l'exercice dans une iframe
    Note over M,E : L'élève effectue l'exercice
    E ->> S : L'exerciseur remonte le score à la<br />fenêtre parente via l'api postMessage
    S ->> M : Mon script change la valeur du<br />champs de réponse avec le score obtenu
    #Note over M,S :
    -->
<img src="https://mermaid.ink/svg/pako:eNp1U8tu2zAQ_JUFe_DFRe9GYSBIfbN68dWXNTmyCVAkw4eQIMi_9NjkN_RjISXVVppWB4na18zOLp-FdApiIyIeMqzED83nwN3RUnk4J2dzd0KY_j2HpKX2bBM1xJEa55TBZ-dhclqKMmifPgfsasB-hUcEqSPyDPDlp0sg1yNQsz7QhvZMhVdMutQqH8oWN4MCpSdfXnhM1awLYTIa-fsp0LdtcUtnE6wOpPIcxT3kxyo1RsPW2h_oNvR1u6VK4q5ttbyAzIJMRZMXDmdQd-1zwkUig0jati5SzIHM3KcEDb_mrLnhwwjSFJB7HiFQ_Z2PtbkwvHpnI-p5id2NqtOywq5WmOiYVQ5mTLnBKrZx7Fq3ZbjzwJZa1_z9ang1w-8ehLaFTHlZYkrZXTVZzo4Cuip0ZR-lC2Obhic1WtjhLRVbGT9qUK-51GWvybuYGsTIZ_ytxm13qh72PArQs6loap7vP4Qap3tl4U5l-Pk_myXWokPoWKuy_c816CjSBUUcsSlHhZazSUdxtC8ltN6Ew5OVYpNCxlpkrzj9uSyT8eUd2ZEgKg" />