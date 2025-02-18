---
title: 在云函数中使用环境变量
---

# {{ $frontmatter.title }}

## 添加环境变量

1. 首先点击页面左下角的小齿轮按钮，打开应用设置页面。
2. 其次在弹出的应用设置界面，点击环境变量，在下方新起一行输入你的环境变量。格式为：`NAME='value'`
3. 点击更新生效。  

## 使用环境变量

环境变量添加完成后，即可在任意云函数中通过访问 `process.env` 来使用。

:::tip
 `cloud.env` 已废弃
:::

```typescript
import cloud from '@lafjs/cloud'

export async function main(ctx: FunctionContext) {
  
    const env = process.env
    console.log(env)
    // 所有的环境变量都在 process.env 里面
}
```
