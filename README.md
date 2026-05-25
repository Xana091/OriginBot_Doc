# OriginBot_Doc
OriginBot pro 智慧医疗赛题
# OriginBot 校赛仓库



## 比赛流程
P点发车 → 避障行驶到任务发布点 → 识别二维码+图文牌并语音播报 → 按二维码方向绕黄色通道一圈 → 返回P点停车

## 仓库结构
- obstacle_avoidance/avoid.py - B负责：避障
- qr_code/detect.py - C负责：二维码识别
- voice/speak.py - C负责：语音播报
- line_following/follow.py - D负责：沿黄线巡线
- main_race/race_flow.py - A负责：主流程串联
- videos/ - 测试录屏
- README.md - 本文件

## 协作规则
1. 每人只改自己文件夹里的代码
2. 每天10点前 push 到 GitHub
3. A实车测试，录屏发群里
4. 自己写的bug自己修
