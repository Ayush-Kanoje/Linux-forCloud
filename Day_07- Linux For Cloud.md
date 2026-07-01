📌 𝗗𝗮𝘆 𝟳 𝗼𝗳 𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴 𝗟𝗶𝗻𝘂𝘅 𝗳𝗼𝗿 𝗖𝗹𝗼𝘂𝗱

Today, I focused on four commands that may seem basic, but they’re the ones you keep reaching for when parsing logs, handling data, or building quick automation scripts.

𝟏. 𝐰𝐜 — 

wc stands for word count, but under the hood, it’s a simple parser that walks through the file byte by byte, counting:

   • newline characters → lines

   • whitespace-separated tokens → words

   • total bytes → size

It doesn’t load the whole file into memory — it streams the data. That’s why it works even on massive log files.

 🔹𝐈𝐧 𝐩𝐫𝐚𝐜𝐭𝐢𝐜𝐞:
      i. wc myfile.txt

𝟐. 𝐜𝐮𝐭 —

cut follows the Unix principle: operate on structured text and extract only what you need. It doesn’t “understand” CSV or logs — it simply slices text based on:

         • delimiter (-d)

         • byte position (-b)

         • character position (-c)

         • field number (-f)

It’s fast because it doesn’t parse or interpret — it just cuts based on positions.

🔹𝐈𝐧 𝐩𝐫𝐚𝐜𝐭𝐢𝐜𝐞:
     i. cut -b 1-4 myfile.txt  

𝟑. 𝐭𝐞𝐞 —

At a system level, tee literally splits the input stream into two outputs:

         • one goes to STDOUT (so you can see it)

         • one goes to a file descriptor (so it gets saved)

It’s basically a fork for data streams. 

🔹𝐈𝐧 𝐩𝐫𝐚𝐜𝐭𝐢𝐜𝐞:
     i. echo "hello" | tee file.txt
