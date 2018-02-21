# linux
Notes linux

1. Finding largest directories and files in Linux
du -ah /* 2>/dev/null | sort -rh | head -n 10

2. Finding the top largest directories in Linux
du -sh /*/ 2>/dev/null | sort -rh | head -n 10
find /var/* -type d -exec du -sh {} 2>/dev/null + | sort -rh | head -n 10

3. Finding the top largest files in Linux
find / -type f -exec du -sh {} 2>/dev/null + | sort -rh | head -n 10

4. Finding the largest files with a specific extension in Linux
find / -type f -iname "*.deb" -exec du -sh {} + | sort -rh | head -10
Source https://www.rosehosting.com/blog/find-large-files-linux/

