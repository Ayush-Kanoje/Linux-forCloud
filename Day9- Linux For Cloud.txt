📌 𝐃𝐚𝐲 𝟗 𝐨𝐟 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐋𝐢𝐧𝐮𝐱 𝐟𝐨𝐫 𝐂𝐥𝐨𝐮𝐝 — 𝐔𝐧𝐝𝐞𝐫𝐬𝐭𝐚𝐧𝐝𝐢𝐧𝐠 𝐊𝐞𝐲 𝐒𝐲𝐬𝐭𝐞𝐦 𝐃𝐢𝐫𝐞𝐜𝐭𝐨𝐫𝐢𝐞𝐬.
Today I dug into some of the core directories that make a Linux system actually work. These folders aren’t random—they control how the OS runs, stores data, and manages users. Once you understand them, Linux stops feeling like a maze.
𝟭. /𝗯𝗶𝗻 — 𝗘𝘀𝘀𝗲𝗻𝘁𝗶𝗮𝗹 𝗨𝘀𝗲𝗿 𝗖𝗼𝗺𝗺𝗮𝗻𝗱𝘀
These commands must always be available, even when the system is running in recovery or single-user mode.
Typical binaries here:
 • ls, cat, cp, mv, grep, bash
🔹𝗪𝗵𝘆 𝗶𝘁 𝗺𝗮𝘁𝘁𝗲𝗿𝘀:
 • These tools are required during boot and maintenance.
 • If /bin breaks, many core functions will fail.
𝟮. /𝗲𝘁𝗰 — 𝗦𝘆𝘀𝘁𝗲𝗺 𝗖𝗼𝗻𝗳𝗶𝗴𝘂𝗿𝗮𝘁𝗶𝗼𝗻 
/etc is where Linux stores system-wide configuration files.
Everything that controls your system’s behaviour sits here.
Common things inside /etc:
 • Network configs → /etc/network/
 • User account info → /etc/passwd, /etc/shadow
 • Service settings → /etc/systemd/
 • Host and DNS configs → /etc/hosts, /etc/resolv.conf
 • File system mount rules → /etc/fstab
🔹𝗪𝗵𝘆 𝗶𝘁 𝗺𝗮𝘁𝘁𝗲𝗿𝘀:
 • If you misconfigure a file, your network, boot process, or services can break.
 • If you know what you’re doing, you can shape exactly how your system operates.
𝟯. /𝗵𝗼𝗺𝗲 — 𝗨𝘀𝗲𝗿 𝗪𝗼𝗿𝗸𝘀𝗽𝗮𝗰𝗲
Every user gets a personal directory inside /home.
This is where user files are alive, like:
 • Documents
 • Downloads
 • Scripts
 • Personal configs
🔹𝗪𝗵𝘆 𝗶𝘁 𝗺𝗮𝘁𝘁𝗲𝗿𝘀:
 • Backups usually include /home to protect personal files.
𝟰. /𝗿𝗼𝗼𝘁 — 𝗔𝗱𝗺𝗶𝗻𝗶𝘀𝘁𝗿𝗮𝘁𝗼𝗿’𝘀 𝗛𝗼𝗺𝗲 𝗗𝗶𝗿𝗲𝗰𝘁𝗼𝗿𝘆
Not to be confused with / (root of filesystem).
/root is the root user’s private home directory.
Key points:
 • Only the superuser should access it.
 • System-wide maintenance scripts might drop logs or configuration backups here.
 • It is separate from /home for security reasons.
🔹𝗪𝗵𝘆 𝗶𝘁 𝗺𝗮𝘁𝘁𝗲𝗿𝘀:
 • Any mistake as the root affects the whole system, not just one user.
𝟱. /𝘃𝗮𝗿 — 𝗖𝗼𝗻𝘀𝘁𝗮𝗻𝘁𝗹𝘆 𝗖𝗵𝗮𝗻𝗴𝗶𝗻𝗴 𝗗𝗮𝘁𝗮
/var stores data that grows or changes over time.
Common subdirectories:
• /var/log/ → System and service logs
• /var/lib/ → Databases and service state
• /var/cache/ → Cached files
• /var/spool/ → Print jobs, mail queues
🔹𝗪𝗵𝘆 𝗶𝘁 𝗺𝗮𝘁𝘁𝗲𝗿𝘀:
 • Logs can fill up disk space.
 • Servers rely heavily on /var to store runtime data.
 • If /var is full, the system can slow down or block processes.