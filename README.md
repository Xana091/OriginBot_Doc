# OriginBot_Doc
OriginBot pro 智慧医疗赛题


# OriginBot 校赛仓库



## 比赛流程
P点发车 → 避障行驶到任务发布点 → 识别二维码+图文牌并语音播报 → 按二维码方向绕黄色通道一圈 → 返回P点停车

## 仓库结构

```

src/
├── obstacle_avoidance/
│   └── avoid.py          # B负责：避障行驶
├── qr_code/
│   └── detect.py         # C负责：二维码识别
├── voice/
│   └── speak.py          # C负责：语音播报
├── line_following/
│   └── follow.py         # D负责：沿黄线巡线
└── main/
└── race_flow.py      # A负责：主流程串联

```

## 分工表

| 文件夹 | 负责人 | 任务 | 输入 | 输出 |
|--------|--------|------|------|------|
| `obstacle_avoidance/` | B | 避障行驶到任务发布点 | 激光雷达 | 速度指令 |
| `qr_code/` | C | 识别二维码方向 | 摄像头图像 | left / right |
| `voice/` | C | 语音播报识别结果 | 文字 | 语音输出 |
| `line_following/` | D | 沿黄色通道巡线一圈 | 摄像头图像 | 速度指令 |
| `main/` | A | 串联整个流程 | 各模块结果 | 完整运行 |

## 协作规则

1. 每人只改自己文件夹里的代码
2. 每天 22:00 前 push 到 GitHub
3. A在实车上测试，录屏发群里
4. 自己写的 bug 自己修

## 如何开始

```bash
# 克隆仓库
git clone https://github.com/你的用户名/OriginBot_Doc.git

# 进入目录
cd OriginBot_Doc

# 每个人进入自己的文件夹写代码

