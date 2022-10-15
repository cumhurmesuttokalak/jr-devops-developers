# jr-devops-developers
# Steps 
# Your local
1. Create a new project and open it with vscode <br>
2. Clone repository to your computer <br>
`github.com/jotform/frontend.git` <br>
3. Create a folder named .vscode in your project and inside this folder create a file named sftp.json <br>
4. Configre the sftp.json under .vscode/sftp.config.json by changing the #USERNAME# fields with the username provided to you. If you configured SSH with the automated script, you need to change ~/.ssh/id_rsa to ~/.ssh/id_jotform <br> <br>
<img width="1440" alt="Ekran Resmi 2022-08-23 17 45 07" src="https://user-images.githubusercontent.com/79723267/186188763-6746377d-9c8e-4317-8431-88a178391028.png"> <br>
5. Check your project <br>
`git checkout jr-devops-developers_nomerge`
6. Execute sync command and transfer local files to your RDS `./sync` <br>
# RDS <br>
7. Create a new terminal and connect to RDS <br>
`ssh username@ssh.jotform.dev` <br>
8. Go to path /www/frontend/username <br>
`cd /www/frontend/username` <br>
9. Install javascript dependencies using pnpm <br>
  `pnpm install` <br>
10. Let NX configure your project with our bootstrap command <br>
  `pnpm build:all` <br>
11. Open a new screen <br>
`screen -S {screen name}` <br>
12. You are ready to go! Simply start desired project with our jf tool <br>
`pnpm jf start dev-tools` <br>
13. You can access desired project on RDS via following link `https://{username}.jotform.dev/f/{projectName}`if project does not have any reserved path like workflow, inbox etc. <br>











