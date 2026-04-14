# Encrypt Page

一个可视化的内容加密/解密页面，适用于 GitHub Pages 静态部署。

## 功能

- AES-256-CBC 加密
- AES-256-CBC 解密
- 密文格式：`ivHex:cipherHex`
- 一键复制结果、错误提示

## 使用要求

- 密钥按 UTF-8 输入，最少 1 字节；实际使用时会先进行 SHA-256 派生为 32 字节 AES 密钥
- 解密输入必须是 `ivHex:cipherHex` 格式

## 本地预览

直接双击 `index.html` 或使用任意静态服务器：

```bash
python3 -m http.server 8080
```

然后访问 `http://localhost:8080`。

## 部署到 GitHub Pages

1. 提交代码到仓库默认分支（如 `main`）
2. 打开仓库 Settings -> Pages
3. Source 选择 `Deploy from a branch`
4. Branch 选择 `main`，目录选择 `/ (root)`
5. 保存后等待部署完成，访问生成的页面地址
