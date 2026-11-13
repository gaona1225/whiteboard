# Whiteboard

实时协同白板（作品集项目三）。重点：工程深度——实时同步、画布性能。

## 技术选型
- Next.js 13.5.6（App Router）+ TypeScript + React 18
- Yjs + Hocuspocus（同步服务器自搭）
- MongoDB Atlas M0（持久化）
- 仅 PC 端，不登录，访客身份

## 目录结构
```
whiteboard/
├── src/
│   ├── app/
│   │   ├── page.tsx              # 首页（最近房间列表）
│   │   ├── layout.tsx
│   │   ├── globals.css
│   │   ├── room/
│   │   │   └── [name]/
│   │   │       └── page.tsx      # 白板房间页
│   │   └── admin/
│   │       └── page.tsx          # 管理页 /admin
│   ├── components/               # 画布、工具栏、头像、弹层等
│   ├── lib/                      # Yjs 文档模型、房间、工具函数
│   └── types/                    # 类型定义
├── server/
│   └── index.js                  # 同步服务器入口（Phase 2 接 Hocuspocus）
├── public/
├── package.json
└── README.md
```

## 本地运行
需要两个终端窗口：
```bash
npm run dev     # 前端 + API，http://localhost:3000
npm run server  # 同步服务器，端口 1234
```

## 部署
演示视频 + 本地运行（不用 Vercel/Railway）。
