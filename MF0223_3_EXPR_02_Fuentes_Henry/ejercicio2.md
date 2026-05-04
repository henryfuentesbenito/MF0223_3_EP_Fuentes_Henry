    1  ls /var/empresa
    2  cat /var/empresa/prueba.txt
    3  exit
    4  pwd
    5  ls
    6  cd /home
    7  cd
    8  cd /var/empresa
    9  mkdir dev_environment
   10  ls
   11  cd dev_environment
   12  mkdir -p frontend/{public,src/{components,pages,styles}} backend/{app,config,tests} database/migrations docs scripts
   13  ls
   14  find . -type d
   15  touch frontend/public/index.html
   16  ls frontend/public
   17  touch frontend/src/App.js
   18  ls frontend/src
   19  touch frontend/src/styles/main.css
   20  ls frontend/src/styles
   21  touch backend/app/server.js
   22  ls backend/app
   23  touch backend/config/config.json
   24  ls backend/config
   25  touch README.md
   26  ls
   27  touch scripts/deploy.sh
   28  ls scripts
   29  apt update
   30  apt install nano -y
   31  nano --version
   32  nano frontend/public/index.html
   33  nano frontend/src/App.js
   34  nano frontend/src/styles/main.css
   35  ls -R
   36  ls -la
   37  ls frontend/src
   38  mkdir backup
   39  ls
   40  cp -r frontend backup/
   41  ls backup
   42  cp backend/app/server.js backup/server_backup.js
   43  ls backup
   44  mv frontend/src/styles/main.css frontend/public/
   45  ls frontend/public
   46  mv frontend/src/App.js frontend/src/app.js
   47  ls frontend/src
   48  mv backend/config/config.json backend/app/
   49  ls backend/app
   50  chmod 700 scripts/deploy.sh
   51  ls -l scripts/deploy.sh
   52  chmod 640 backend/app/server.js
   53  ls -l backend/app/server.js
   54  chmod 444 README.md
   55  ls -l README.md
   56  ls -l scripts/deploy.sh backend/app/server.js README.md
   57  rm -r frontend/src/components
   58  ls frontend/src
   59  cp -r backup/frontend/src/components frontend/src/
   60  ls frontend/src
   61  ls -l frontend/src
   62  ls
   63  rm backup/server_backup.js
   64  ls backup
   65  ls -R
   66  pwd
   67  history