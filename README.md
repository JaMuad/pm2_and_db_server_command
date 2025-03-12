# Notes


1) This file inside the Backend repo was used to automate and create the db. You have to run it on the ec2 instance server.
```Prograde-Backend/ create gg-database-and-user.sh```

2) Next thing you confirm the running apps on the server. 
```pm2 list```

3) If you have a corrupted Database set up you just do. 
```psql -U gradific -C "DROP DATABASE gradific_staging"```

4) You move into the project directory, cd gradific/staging.

5) ls to view that your project content is inside here.

6) Add the db script file into the project for it to be run, then you copy the content from your project file Prograde-Backend/ create gg-database-and-user.sh and paste inside the setup.sh
```sudo nano setupdb.sh``` COPY `Prograde-Backend/ create gg-database-and-user.sh` into `setupdb.sh`

7) The command `chmod +x` `setupdb.sh` makes the `setupdb.sh` file executable, allowing it to be run as a script.
```sudo chmod  +x setupdb.sh```

8) Run the server
```./setupdb.sh```

- Then a prompt will pop up and you enter password
- Do you want want to use an existing user? (y/n) = y
- Should this user be the owner of the database? (y/n) = y