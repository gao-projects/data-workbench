# 重新构建环境

编译顺序：3rdparty, src, plugins

C2665  qHash 
重写自定义类型qHash DNAbstractNode DNAbstractNodeFactory

pybind11 : 由于QT中定义了slots作为关键了，而python3中有使用slot作为变量，所以有冲突。
```
#undef slots //这里添加
typedef struct{
    const char* name;
    int basicsize;
    int itemsize;
    unsigned int flags;
    PyType_Slot *slots; /* terminated by slot==0. */
} PyType_Spec;
#define slots Q_SLOTS //这里添加
```

