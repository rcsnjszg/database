# Adatbázis

Az adatbázis kezeléshez szükséges *mysql*, és egy vele együttműködő *phpmyadmin* docker compose segítségével összeállítva.

Az adatbázis adatait volume-ban tárolja.

## Indítás

```bash
docker-compose up -d
```

## Leállítás

```bash
docker compose stop
```

## Eltávolítás

Ha nincs szükségünk az adatbázisra, vagy valami miatt el kell távolítani, akkor az alábbi utasítás alkalmazható

```bash
doker compose down -v
```

 - A `-v` a volume-ot is eltávolítja

**Figyelem!** Az adatbázis látszólag elindult és használható, de még 1-2 perc várakozás szükséges lehet mielőtt tényleg használatba vehető állapotba kerül!

## Belépés PHP MyAdminból

 - A phpmyadmin alapértelmezés szerint a http://localhost:8080 címen érhető el
 - A `root` felhasználóval lehet belépni, akinek az alapértelmezett jelszava: `root_p_ssW0rd`
 
 Mivel a phpmyadmin és az adatbázis konténerei belső hálózaton kommunikálnak egymással, így a host `localhost` helyett `db` lesz.

## Csatlakozás külső programból

 - Host: `localhost`
 - Port: `3306`
 - Username: `root`
 - Password: `root_p_ssW0rd`