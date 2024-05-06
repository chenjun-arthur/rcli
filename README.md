# RCLI

rcli is a rust cli tool
Directly add class notes here

# Notes

## v1-09-base64

单元测试相关命令
```bash
# 对于项目内所有的test进行测试
cargo nextest run

# 只针对某个函数进行测试
cargo nextest run -- test_verify_input_file
```

```bash
# 依赖添加相关命令
cargo add base64
```

```bash
# 执行后，需要按Ctrl + D才会输出结果
cargo run -- base64 encode --format urlsafe
cargo run -- base64 decode --format urlsafe
```

```bash
# 直接进行文件的输入执行
cargo run -- base64 encode --format urlsafe -i Cargo.toml > tmp.64
cargo run -- base64 decode --format urlsafe -i tmp.64
```

- 版本发布
```bash
git tag -a v1-9-base64
```

- IDE Setting 使得VS code在保存文件的时候，能够对于依赖自动进行排序，而且在一行过长的时候，能够自动进行换行
    - 在settings.json中增加如下字段
```json
    "[rust]": {
        "editor.defaultFormatter": "rust-lang.rust-analyzer",
        "editor.formatOnSave": true,
    },
```

    - 看起来对于单独的workspace或者工程环境，可以配置settings.json，从Setting选项页面的右上角图标就可以进入文本化的配置文件；
