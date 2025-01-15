# 汉字拼音查询包 (Pinyin-Dict)

[English](README_en.md)

## 描述
`pinyin-dict` 是一个用于查询汉字拼音（罗马化）的包。它提供了获取简体和详细拼音表示的工具。

## 安装
你可以使用 npm，pnpm 或 yarn 来安装这个包：

```bash
npm install pinyin-dict
```
```bash
pnpm add pinyin-dict
```
```bash
yarn add pinyin-dict
```

## 使用方法

### 导入包
你可以按以下方式从包中导入函数：

```typescript
import { pinyin, detailedPinyin, all } from 'pinyin-dict';
```

### 函数

#### `pinyin(char: string): string[] | undefined`
返回给定汉字的拼音表示数组，不带声调。

**示例:**
```typescript
const result = pinyin('汉'); // ['han']
console.log(result);
```

#### `detailedPinyin(char: string): string[] | undefined`
返回给定汉字的详细拼音表示数组，包括声调。

**示例:**
```typescript
const result = detailedPinyin('汉'); // ['hàn']
console.log(result);
```

#### `all(): Readonly<typeof dict>`
返回整个汉字到含声调拼音映射的字典。

**示例:**
```typescript
const dict = all();
console.log(dict['汉']); // ['hàn']
```

## 数据来源

本包中的数据来源为：[汉文学网](https://zd.hwxnet.com/)

爬取脚本可见 `cmd/fetcher.ts`

## 许可证
本包采用 MIT 许可证。

## 贡献
欢迎贡献！请提交问题或拉取请求。

## 作者
- Neooier