# Adatbázis

Az adatbázis kezeléshez szükséges *mysql*, és egy vele együttműködő *phpmyadmin* docker compose segítségével összeállítva.

Az adatbázis adatait a gépen tárolja a `/docker/mysql/var/lib/mysql` mappában.


## Indítás

```bash
docker-compose up -d
```

**Figyelem!** Az adatbázis látszólag elindult és használható, de még 1-2 perc várakozás szükséges lehet mielőtt tényleg használatba vehető állapotba kerül!

## Belépés PHP MyAdminból

 - A phpmyadmin alapértelmezés szerint a http://localhost:8882 címen érhető el
 - A `root` felhasználóval lehet belépni, akinek az alapértelmezett jelszava: `root_password`
 
 Mivel a phpmyadmin és az adatbázis konténerei belső hálózaton kommunikálnak egymással, így a host `localhost` helyett `db` lesz.

## Csatlakozás külső programból

 - Host: `localhost`
 - Port: `33061`
 - Username: `root`
 - Password: `root_password`

Külső csatalkozás esetén a port a mysql alapértelmezett `3306`-os portja helyett itt `33061` lesz, ahogy a `docker-compose.yml` fájlban meg lett határozva.