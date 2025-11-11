📌𝗗𝗮𝘆 𝟰 𝗼𝗳 𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴 𝗟𝗶𝗻𝘂𝘅 𝗳𝗼𝗿 𝗖𝗹𝗼𝘂𝗱 — 𝐃𝐨𝐢𝐧𝐠 𝐑𝐞𝐚𝐥 𝐖𝐨𝐫𝐤 𝐢𝐧 𝐋𝐢𝐧𝐮𝐱
Every Cloud engineer spends a huge part of their day navigating through servers, managing files, and checking configurations.
Today, I practised the Linux commands that make this possible —
𝟏. 𝐌𝐨𝐯𝐢𝐧𝐠 𝐀𝐫𝐨𝐮𝐧𝐝 𝐰𝐢𝐭𝐡 𝐜𝐝 (𝐜𝐡𝐚𝐧𝐠𝐞 𝐝𝐢𝐫𝐞𝐜𝐭𝐨𝐫𝐲)
cd lets you move between directories (folders) in your Linux system.
       • cd /home/user → moves into the user directory.
       • cd ..  → move user back to previous folder.
       • cd ~ → takes you back to your home directory.
🔹Use case: When managing multiple EC2 apps or Docker setups, you’ll frequently switch between folders — /var/logs, /etc/nginx, /home/ec2-user/app — to configure or debug systems

𝟐. 𝐂𝐫𝐞𝐚𝐭𝐞 𝐅𝐨𝐥𝐝𝐞𝐫 𝐮𝐬𝐢𝐧𝐠 𝐦𝐤𝐝𝐢𝐫 (𝐦𝐚𝐤𝐞 𝐝𝐢𝐫𝐞𝐜𝐭𝐨𝐫𝐲)
mkdir creates new directories.
       • mkdir projects → creates a folder named projects. 
       • mkdir -p dev/scripts → creates nested directories in one go.
 🔹Use case: When preparing different environments (Dev, Staging, Prod) in AWS or GCP, this command helps organize deployment and config files neatly.

𝟑. 𝐂𝐫𝐞𝐚𝐭𝐢𝐧𝐠 𝐅𝐢𝐥𝐞𝐬 𝐰𝐢𝐭𝐡 𝐭𝐨𝐮𝐜𝐡
touch creates empty files or updates file timestamps.
       • touch notes.txt → creates an empty text file.
       • touch deploy.log → creates deployment logs files.
🔹Use case: When automating deployments or backups using cron jobs or CI/CD, you often create log files before writing data into them.

𝟒. 𝐂𝐥𝐞𝐚𝐧𝐢𝐧𝐠 𝐔𝐩 𝐭𝐡𝐞 𝐕𝐢𝐞𝐰 𝐰𝐢𝐭𝐡 𝐜𝐥𝐞𝐚𝐫
clear wipes your terminal view clean, giving you a fresh workspace.
        • clear → clears the screen instantly.
 Shortcut: Press 𝘾𝙩𝙧𝙡 + 𝙇 for the same effect.
 
𝟓. 𝐑𝐞𝐚𝐝𝐢𝐧𝐠 𝐅𝐢𝐥𝐞𝐬 𝐰𝐢𝐭𝐡 𝐜𝐚𝐭 𝐚𝐧𝐝 𝐳𝐜𝐚𝐭
Both display file contents directly in the terminal.
        • cat file.txt → prints file content.
        • zcat file.txt.gz → reads compressed .gz files without unzipping.
🔹Use case: Cloud logs like nginx.log.gz or system.log.gz are often compressed to save space — zcat helps read them without manual extraction.

𝐃𝐚𝐲 𝟓 𝐏𝐫𝐞𝐯𝐢𝐞𝐰 — 𝐅𝐢𝐥𝐞 𝐎𝐩𝐞𝐫𝐚𝐭𝐢𝐨𝐧𝐬 & 𝐌𝐨𝐧𝐢𝐭𝐨𝐫𝐢𝐧𝐠
Tomorrow’s focus will be on copying, moving, removing, and inspecting files in real-time, using:
 📁 cp | 🚚 mv | ❌ rm | 🔍 head | 📜 tail | 🔥 tail -f
These are essential for system administration, log monitoring, and real-time debugging in Cloud environments.