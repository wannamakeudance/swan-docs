---
title: command.pop
header: develop
nav: cloud
siderbar: command_pop
---
 
 

**解释**：数据库更新指令，该指令需要操作一个类型为数组的字段，并删除其最后一个元素。

**代码示例**

```js
    swan.cloud.init({
        env: 'envId'
    });
    const db = swan.cloud.database();
    const _ = db.command;
    db.collection('users')
      .doc('docId')
      .update({
          tags: _.pop()
      })
```

