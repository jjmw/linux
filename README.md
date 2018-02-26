# linux
Notes linux

1. Finding largest directories and files in Linux
```bash
du -ah /* 2>/dev/null | sort -rh | head -n 10
```

2. Finding the top largest directories in Linux
```bash
du -sh /*/ 2>/dev/null | sort -rh | head -n 10
```
```bash
find /var/* -type d -exec du -sh {} 2>/dev/null + | sort -rh | head -n 10
```

3. Finding the top largest files in Linux
```bash
find / -type f -exec du -sh {} 2>/dev/null + | sort -rh | head -n 10
```

4. Finding the largest files with a specific extension in Linux
```bash
find / -type f -iname "*.deb" -exec du -sh {} + | sort -rh | head -10
```
[Source](https://www.rosehosting.com/blog/find-large-files-linux/)

5. create tar file; multiple files/paths
- tar -cvf file_name.tar <path_to_directory>
- tar -cvf file_name.tar <path_to_file1> <path_to_file2> <path_to_file3>
    c. – Create a new .tar archive file
    v. – Verbose mode to show the files being progressed
    f. – Name of the archive file (can be STDOUT if the filename is replaced by -)
