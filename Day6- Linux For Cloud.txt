📌 𝐃𝐚𝐲 𝟔 𝐨𝐟 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐋𝐢𝐧𝐮𝐱 𝐟𝐨𝐫 𝐂𝐥𝐨𝐮𝐝 — 𝐇𝐚𝐫𝐝𝐥𝐢𝐧𝐤 & 𝐒𝐨𝐟𝐭𝐥𝐢𝐧𝐤
Today, I finally sat down and cleaned up my understanding of how Linux treats files, especially the whole Hardlink vs Softlink confusion. 
𝟭. 𝗛𝗮𝗿𝗱𝗹𝗶𝗻𝗸 — 𝗔𝗻𝗼𝘁𝗵𝗲𝗿 𝗡𝗮𝗺𝗲 𝗳𝗼𝗿 𝘁𝗵𝗲 𝗦𝗮𝗺𝗲 𝗙𝗶𝗹𝗲
A hardlink points to the same inode, meaning the same data on disk.
 It’s not a shortcut. It’s not a copy. It’s literally the same file with another name.
𝗞𝗲𝘆 𝗽𝗼𝗶𝗻𝘁𝘀:
 • Hardlink survives even if you delete the “original” file
 • Works only with files, not directories
 • Cannot work across different filesystems
 • Must be created in the same filesystem where the file already exists
 • Both names have equal priority — there is no “main file” once the hardlink exists
𝗪𝗵𝗲𝗿𝗲 𝘁𝗵𝗶𝘀 𝗶𝘀 𝘂𝘀𝗲𝗳𝘂𝗹:
You need a file reference that never dies, even if someone accidentally deletes the original.

𝟮.𝗦𝗼𝗳𝘁𝗹𝗶𝗻𝗸 (𝗦𝘆𝗺𝗹𝗶𝗻𝗸) — 𝗔 𝗣𝗮𝘁𝗵 𝗥𝗲𝗱𝗶𝗿𝗲𝗰𝘁
Softlinks are the more flexible option, but also more fragile.
A softlink stores a path, and Linux simply follows that path.
𝗞𝗲𝘆 𝗽𝗼𝗶𝗻𝘁𝘀:
 • Can link files, folders, broken paths, even other symlinks
 • Works across filesystems
 • If the target file is moved → the symlink breaks
 • You can only 𝗰𝗱 into it if the link points to a directory
 • Editing a file through a symlink still edits the original file
𝗪𝗵𝗲𝗿𝗲 𝘁𝗵𝗶𝘀 𝗶𝘀 𝘂𝘀𝗲𝗳𝘂𝗹:
Organising messy folder structures, linking configs, or giving consistent names to files regardless of where they move.

🔹 𝗪𝗵𝗶𝗰𝗵 𝗢𝗽𝗲𝗿𝗮𝘁𝗶𝗼𝗻𝘀 𝗔𝗿𝗲 𝗣𝗼𝘀𝘀𝗶𝗯𝗹𝗲?
If the original file exists:
 • Read
 • Write
 • Edit
 • Open
Hardlink or softlink — both will work smoothly.
𝗜𝗳 𝘁𝗵𝗲 𝗼𝗿𝗶𝗴𝗶𝗻𝗮𝗹 𝗳𝗶𝗹𝗲 𝗶𝘀 𝗱𝗲𝗹𝗲𝘁𝗲𝗱:
 • Hardlink: still works (data is still there)
 • Softlink: becomes broken (path is dead)
𝗜𝗳 𝘁𝗵𝗲 𝗼𝗿𝗶𝗴𝗶𝗻𝗮𝗹 𝗳𝗶𝗹𝗲 𝗶𝘀 𝗺𝗼𝘃𝗲𝗱:
 • Hardlink: still works
 • Softlink: breaks unless you update its path
This is the part most beginners completely misunderstand — and then wonder why their symlinks suddenly “stop working.”