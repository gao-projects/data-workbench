# ���¹�������

����˳��3rdparty, src, plugins

C2665  qHash 
��д�Զ�������qHash DNAbstractNode DNAbstractNodeFactory

pybind11 : ����QT�ж�����slots��Ϊ�ؼ��ˣ���python3����ʹ��slot��Ϊ�����������г�ͻ��
```
#undef slots //�������
typedef struct{
    const char* name;
    int basicsize;
    int itemsize;
    unsigned int flags;
    PyType_Slot *slots; /* terminated by slot==0. */
} PyType_Spec;
#define slots Q_SLOTS //�������
```

