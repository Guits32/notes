Deux options:
- mise en place d'un NAS: permet d'avoir un stockage distant 
- mise en place d'un d'un serveur de backup: rigide consistent et sécurisé

### Dedup des disques actuels

Logiciel de dedup: 
- à mon avis la meilleure option - [Duplicate File Finder](https://www.auslogics.com/en/software/duplicate-file-finder/)
- autre bonne option je pense - [Cuplicate Cleaner](https://www.pcastuces.com/logitheque/duplicate_cleaner.htm)
- sinon voir dans ces logiciels [là](https://www.ionos.com/digitalguide/server/know-how/finding-duplicate-files-in-windows/) 

### Système de backup

#### Hardware

Pour le serveur (`backup-server` sur le schéma) qui va être responsable du backup:
- pour les connectiques sur la carte mère:
	- doc de perf:
		- sata [ici](https://support-fr.wd.com/app/answers/detailweb/a_id/39798/~/diff%C3%A9rence-entre-sata-i%2C-sata-ii-et-sata-iii)
		- usb [ici](https://tripplite.eaton.com/products/usb-connectivity-types-standards#usb-standards)
	- option la plus performantes (mais surement overkill): 2 ports SATA  III
	- option valables:
		- 2 ports SATA II
		- 2 ports SATA I
		- 2 ports usb 3 dédiés aux DD
	- options à exclure:
		- partager une connectique pour les 2 DD
- pour la RAM:
	- option optimale >= 8GB
	- option acceptable: 4GB
	- option non valable < 4GB
- pour le CPU
	- 2/4 cores
	- base frequency >= 1.5GHz

#### Schéma

[[assets/backup-server_simon.excalidraw]]

![[backup_simon.png]]


### Système NAS

