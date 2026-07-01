📌𝐃𝐚𝐲 𝟖 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐋𝐢𝐧𝐮𝐱 𝐅𝐨𝐫 𝐂𝐥𝐨𝐮𝐝  — 𝐅𝐢𝐥𝐞_𝐒𝐲𝐬𝐭𝐞𝐦
Today I focused on understanding how Linux actually stores files, not just how to move them around with commands. I always thought a “file system” was just a folder structure, but it’s way deeper than that.
The main thing I learned is this:
"𝐋𝐢𝐧𝐮𝐱 𝐝𝐨𝐞𝐬𝐧’𝐭 𝐜𝐚𝐫𝐞 𝐚𝐛𝐨𝐮𝐭 𝐟𝐢𝐥𝐞𝐧𝐚𝐦𝐞𝐬. 𝐈𝐭 𝐜𝐚𝐫𝐞𝐬 𝐚𝐛𝐨𝐮𝐭 𝐢𝐧𝐨𝐝𝐞𝐬."
𝟭.𝗪𝗵𝗮𝘁 𝗮 𝗙𝗶𝗹𝗲 𝗦𝘆𝘀𝘁𝗲𝗺 
 -> A file system in Linux controls how files and directories are stored, organized, and found on the disk.
 🔹It’s structure decides:
 • Where your file data sits on disk
 • How it’s located
 • How fast it can be accessed
 • How safe it is from corruption
 Q. How check our Linux file system? (using cmd)
 -> i. lsblk -f
 ii. df -Th
 🔹𝗧𝘆𝗽𝗲𝘀 𝗼𝗳 𝗙𝗶𝗹𝗲 𝗦𝘆𝘀𝘁𝗲𝗺 𝗶𝗻 𝗟𝗶𝗻𝘂𝘅
 • EXT4, XFS, Btrfs, EXT3/EXT2, FAT32/exFAT, NTFS, ZFS.
File system types matter because they determine speed, reliability, features, and how safe your data is.
𝟮. 𝗜𝗻𝗼𝗱𝗲𝘀 — 𝘁𝗵𝗲 𝗔𝗰𝘁𝘂𝗮𝗹 𝗜𝗱𝗲𝗻𝘁𝗶𝘁𝘆 𝗼𝗳 𝗮 𝗙𝗶𝗹𝗲
 -> An inode is like a file’s identity card in Linux — it stores everything about the file except its name, including where the file’s actual data is located on the disk.
🔜 𝗪𝗵𝗮𝘁 𝗜’𝗺 𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴 𝗧𝗼𝗺𝗼𝗿𝗿𝗼𝘄 (𝗗𝗮𝘆 𝟵 𝗣𝗿𝗲𝘃𝗶𝗲𝘄)
Tomorrow I’m focusing on the key Linux directories — /bin, /root, /etc, and a few others.
