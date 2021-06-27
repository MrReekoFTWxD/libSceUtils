# File System

## Write File
```
//Writing string to file
write_file("path", "Example", strlen("Example"));

//Writing buffer to file
char buffer[5] = {1,1,1,1,1};
write_file("path", buffer, sizeof(buffer));
```

## Reading File
```
char buffer[0x400];
size_t fileSize;

read_file("path", buffer, sizeof(buffer), &fileSize);
```

## Make Directory
```
make_directory("path");
```

## Check if file exist
```
if(file_exist("path"))
    ThingToDoIfFileDoesExist();
```

## Check if directory exist
```
if(directory_exist("path"))
    ThingToDoIfDirectoryDoesExist();
```