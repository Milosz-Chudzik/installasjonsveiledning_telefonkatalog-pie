# laste ned ubuntu og raspberry imager
    1. ta sd-kortet ut av pi-en og putt det inn i laptopen 
    2. gå inn på https://www.raspberrypi.com/software/
    3. velg last ned for ubuntu og vent til den er ferdig
    4. putt sd-kortet inn i pi-en igjen


# oppset av linux:

## 1. Åpne terminalen (ctrl + alt + t)

## 2. oppdater og oppgrader
```
    1. sudo apt update
  
    2. sudo apt uppgrade
```	

## 3. Sette opp brannmur med UFW
```	
    1. sudo apt install ufw
    2. sudo ufw enable
    3. sudo ufw allow ssh
```		
    4. ekstra: du kan sjekke brannmur statusen ved å skrive sudo ufw status

## 4. skru på ssh
```		
    1. sudo apt install openssh-server
    2. sudo systemctl enable ssh
    3. sudo systemctl start ssh
```		

## 5. finn ip-en din
```		
    1. ipa
```		
    2. Hvis du har kablet nettverk, vil IP vises ved eth0: linje. Hvis du kun har trådløst, vil ip vises ved wlan0: linje. IP-adresse er vanligvis 10.2.3.x eller noe lignende.

## 6. installere Git, Python og Mariadb
```
    1. sudo apt install python3-pip
    2. sudo apt install git
    3. sudo apt install mariadb-server
    4. sudo mysql_secure_installation
```

## 7. lage ny database bruker og sette riktige rettigheter
    1. logg inn i maria db 
```	
        sudu mariadb -u root
```

    2. lage ny bruker 
```		
        CREATE USER `username'@'localhost' IDENTIFIED BY 'password';
```		

    3. gi ny bruker rettigheter
```
        GRANT ALL PRIVILEGES ON *.* TO 'username'@’localhost’ IDENTIFIED BY 'password';
```

    4. oppdater rettigher
```
        FlUSH PRIVILEGES;
```

## 8. last ned vscode 
    1. gå inn på nettleseren på raspberrien
    2. gå inn på nettsiden til vscode
    3. last ned vscode for maskinen din

### vis det ikke funker 
    1. Hvis du får trøbbel med VS Code, last ned .deb for arm64 fra https://code.visualstudio.com/docs/setup/linux Naviger til mappen du lastet ned filen

    2. Skriv sudo apt install ./code og trykk tab, så enter

## ferdig 
    1. sudo apt uptdate
    2. sudo apt upgrade


# ssh:
    1. inne på raspberrien skriv ipa 
    2. på laptopen skriv:
```	
    ssh brukernavn@ip
```	

    bytt ut brukernavn og ip med dine