## 修改列表

```sql
a.rename(columns={'A':'a', 'C':'c'}, inplace = True)
```

## join,merge,concat

```sql
data=pd.merge(feature,product,on='cam_id')
cam_info = pd.concat([cam_info2,cam_info1])
```

## 根据一列生成另一列

```sql
infos['rfinfo']=infos['rf_info'].apply(lambda x: x.split('|')[0])
```

## 根据几列生成另一列

```sql
df['col3'] = df.apply(lambda x: x['col1'] + 2 * x['col2'], axis=1)
df['col2'] = df['col1'].map(lambda x: x**2)
```

## 转换类型

```sql
infos[['rf_info']] = infos[['rf_info']].astype('string')
```

## 读写中文乱码问题

```sql
df.to_csv(“sel.csv”, index=False, encoding=”gb2312”) 
```

## 把某个值替换为nan

```sql
a.A.replace(-1,np.nan,inplace=True)
```

## 坐标轴
* axis=0 down
* axis=1 across

## datetime

## 增加默认显示长度

```sql
pd.set_option('max_colwidth',200)
```

## 读取csv指定列名

```sql
df = pd.read_csv(r'D:\project_codes\abc.csv', header=None, names=['a','b','c','d'])
```



