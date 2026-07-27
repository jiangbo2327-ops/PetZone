# 🐾 溜溜爪 PetZone — 宠物服务电商平台

基于 **uni-app + Vue3 + TypeScript + Pinia** 的全端宠物服务电商平台，覆盖微信小程序、H5、App 三端。集商品交易、商家预约、宠物领养于一体。

## 📸 项目预览

| 首页 | 精选商城 | 服务 | 购物车 |
|------|------|------|------|
| ![首页](static/common/images/home.png) | ![精选](static/common/images/sel.png) | ![服务](static/common/images/service.png) | ![我的](static/common/images/me.png) |

## 🛠 技术栈

| 层级 | 技术 |
|------|------|
| 框架 | uni-app (Vue3) |
| 语言 | TypeScript |
| 状态管理 | Pinia 3.x |
| UI 组件库 | uView Plus 3.x |
| CSS 预处理 | SCSS |
| 构建工具 | Vite |
| 日期处理 | dayjs |

| 平台能力 |
|------|
| 微信小程序 — 微信登录、手机号授权、微信支付、LBS 定位 |
| H5 — 腾讯地图 SDK、手机号+短信验证码登录 |
| App (Android/iOS) — 原生定位权限 |

| 第三方服务 |
|------|
| 高德地图 API — GPS 逆地理编码 |
| 腾讯地图 SDK — H5 端地图服务 |

## ✨ 功能模块

- 🏠 **首页** — 城市定位、Banner 轮播、服务分类、商家列表（下拉加载）
- 🛒 **精选商城** — 商品分类浏览（左分类右商品）、规格选择弹窗、加入购物车
- 💼 **服务** — 宠物服务入口、宠物领养、附近商家
- 🛍 **购物车** — 单选/全选、删除商品、动态合计金额
- 📦 **订单结算** — 收货地址管理（省市区三级联动）、订单金额明细、微信支付
- 👤 **个人中心** — 用户信息、我的订单、我的服务、地址管理
- 🔐 **登录** — 微信一键授权登录 / 手机号+短信验证码登录
- 🏪 **商家** — 商家列表（Tab 分类 + 搜索 + 评分/价格排序）、商家详情、服务预约

## 🏗 项目结构

```
liuliuzhua/
├── pages/                  # 主包页面
│   ├── index/             # 首页
│   ├── selected/          # 精选商城
│   ├── service/           # 服务
│   ├── cart/              # 购物车
│   ├── login/             # 登录
│   └── me/                # 个人中心
├── packageA/              # 分包A - 商品详情
│   └── product-detail/
├── packageB/              # 分包B
│   ├── address/           # 地址管理
│   ├── merchant/          # 商家列表
│   ├── merchant-detail/   # 商家详情
│   └── order/             # 订单结算
├── components/            # 公共组件
│   └── products-spec-popup/  # 商品规格弹窗
├── store/                 # Pinia 状态管理
├── utils/
│   ├── http/              # HTTP 请求封装（拦截器）
│   └── getcode.ts         # 高德地图逆地理编码
├── pages.json             # 页面路由 & 分包配置
└── manifest.json          # 应用配置（三端差异化）
```

## 📦 运行

```bash
npm install
```

然后用 HBuilderX 或 uni-app 命令行工具运行到对应平台。

## 📄 License

MIT
