# Idea
[MSDN Docu](https://msdn.microsoft.com/en-us/library/windows/desktop/cc144089(v=vs.85).aspx)

+ rightClick to set Tags on File/Dir
+ option for parse Tags to Chlids
+ when Move File option to keep parent flags
+ menue to filter dir

## TODO:
1. how orenize Flat File System
2. how save FileInfos (keep when copy to other System ?)
3. how modify the FiieExplorer

# Datastriźuctor
## Tagsystem
### Speichern
```c++
std::vector<std::pair<Tag* File*>> // jeder Tag wir oft gespeicrt
calss Tag { // file referenc, troztdem sortierbar
private: std::Vector<File*> _file;
};
```
### Intersection
1. sortierte listsn
2. whlie id[i] > id[i+1], ++id[i+1]
3, eine Liste zuende → return
3. if(id[i] < id[i+1]), ++id[i] goto 2;
4. addTag to Intersection, goto 2;
