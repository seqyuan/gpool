# gpool - Go Goroutine Pool

[![Go Reference](https://pkg.go.dev/badge/github.com/seqyuan/gpool.svg)](https://pkg.go.dev/github.com/seqyuan/gpool)
[![Go Report Card](https://goreportcard.com/badge/github.com/seqyuan/gpool)](https://goreportcard.com/report/github.com/seqyuan/gpool)

A high-performance goroutine pool implementation for Go, providing:

- Dynamic worker pool sizing
- Task queue management
- Panic recovery机制
- 并发安全设计
- 优雅关闭支持

## 安装

```bash
go get github.com/seqyuan/gpool
```

## 快速开始

```go
package main

import (
    "context"
    "github.com/seqyuan/gpool"
)

func main() {
    pool := gpool.NewPool(10) // 初始化10个worker
    defer pool.Close()

    pool.Submit(func(ctx context.Context) {
        // 你的任务逻辑
    })
}
```

## 文档

完整API文档请参考 [GoDoc](https://pkg.go.dev/github.com/seqyuan/gpool)

## 贡献

欢迎提交PR，请遵循以下步骤：
1. Fork仓库
2. 创建特性分支
3. 提交修改
4. 推送分支并创建PR

## 许可证

[MIT License](LICENSE)
