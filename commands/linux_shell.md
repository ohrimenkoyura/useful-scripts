## Commands

#### Port statistic
```
sudo netstat -lpn | grep :8080
```

#### Go to the script's home directory
```
cd ${0%/*} 
```

#### Replace spaces with underscore in names of multiple files or directories
```
find -name "* *" -type d | rename 's/ /_/g'
find -name "* *" -type f | rename 's/ /_/g'
```

#### Get current date in a certain format
```
date '+%Y-%m-%d %H:%M:%S'
```

#### Get uniq set of lines
```
<input> | sort | uniq
or 
<input> | sort -u
```

#### Sort lines of numbers in reverse order
```
<input> | sort -rn
```

#### Kill all processes with a certain name
```
ps aux | awk '/<app>/ {print $2}' | xargs kill
```

### File conversion

#### Merge files line-by-line
```
paste file1.txt file2.txt > fileresults.txt
```

#### Write line to a file
```
echo line > $file_name
```

#### Append line to a file
```
echo line >> $file_name
```

#### Merge files line by line and separate by semicolon
```
paste -d ';' file1.txt file2.txt > merge.txt
```

#### Split file by multiple ones
```
split --additional-suffix=<suffix> --numeric-suffixes -n <count_of_files> <file_name> <output_file_prefix>
```

#### Split file by multiple ones with a sertain lines count
```
split --additional-suffix=<suffix> --numeric-suffixes -l <lines_count> <file_name> <output_file_prefix>
```

#### Split file by chunks that are not larger than 1MB without lines breaking
```
split --additional-suffix=.csv --numeric-suffixes -C 999000 <file_name>.csv <output_file_prefix>
```

#### Convert image from PNG into JPG
```
sudo apt-get install imagemagick
convert image.png image.jpg
```
