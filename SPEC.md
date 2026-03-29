# 小汤的个人网站 - 设计规格

## 1. Concept & Vision

一个富有创意活力和个人特色的设计师个人网站。参考 ATNN Design 的风格——大胆鲜明、年轻有趣、充满能量。整体给人"这就是我"的自信感，色彩活泼但不失专业度。

## 2. Design Language

**美学方向**: 大胆活力主义 + 创意工作室风格，参考 ATNN Design 的鲜明配色与现代布局

**配色方案**:
- Primary Background: `#0D0D0D` (近黑色 - 主背景)
- Secondary Background: `#1A1A1A` (深灰 - 卡片/区块背景)
- Accent Primary: `#FF6B35` (活力橙 - 主要强调)
- Accent Secondary: `#7B2FFF` (电紫色 - 次要强调)
- Accent Tertiary: `#00D4AA` (薄荷绿 - 点缀)
- Text Primary: `#FFFFFF` (白色 - 主文字)
- Text Secondary: `#A0A0A0` (灰色 - 次要文字)

**字体**:
- 标题: `"Space Grotesk", sans-serif` - 现代几何无衬线
- 正文: `"DM Sans", sans-serif` - 清晰现代无衬线

**空间系统**:
- 基础单位: 8px
- 区块间距: 100px - 140px
- 卡片圆角: 24px
- 大圆角: 32px+

**动效哲学**:
- 元素进入视口时滑入 (translateX -50px→0, opacity 0→1, 800ms ease-out)
- 卡片悬停发光边框 (box-shadow glow)
- 文字悬停颜色渐变
- 背景渐变缓慢动画
- 弹性悬停效果 (scale 1.02, 300ms)

## 3. Layout & Structure

**页面结构**:
1. **导航栏** - 左侧Logo + 右侧导航链接，半透明背景
2. **Hero区域** - 全屏，醒目大标题，动态渐变背景装饰
3. **关于我** - 左右分栏，头像 + 个人介绍
4. **作品集** - 卡片网格布局，悬停显示详情
5. **日常** - 瀑布流/不规则网格展示
6. **页脚** - 简洁版权信息

**响应式策略**:
- Desktop (>1024px): 多列布局，大字体
- Tablet (768-1024px): 调整列数，保持视觉冲击
- Mobile (<768px): 单列堆叠，汉堡菜单

## 4. Features & Interactions

**导航**:
- 固定顶部，滚动时背景模糊
- 链接悬停下划线动画
- 移动端全屏菜单

**项目卡片**:
- 悬停时边框发光效果
- 悬停时图片轻微放大
- 显示项目标签

**滚动动画**:
- 元素进入视口时从左侧滑入
- 交错动画延迟

## 5. Component Inventory

**导航栏 (Navbar)**
- Default: 透明背景，白色文字
- Scrolled: 毛玻璃背景
- Mobile: 汉堡图标

**项目卡片 (ProjectCard)**
- Default: 深色背景，圆角，微妙边框
- Hover: 发光边框，scale 1.02

**技能标签 (SkillTag)**
- Default: 胶囊形状，半透明背景
- Hover: 颜色变为强调色

**图片卡片 (ImageCard)**
- Default: 圆角，深色叠加层
- Hover: 叠加层变亮，scale 1.05

## 6. Technical Approach

- 单页HTML + 内联CSS + Vanilla JavaScript
- CSS Grid + Flexbox 布局
- Intersection Observer API 实现滚动动画
- CSS Custom Properties 管理主题
- Google Fonts 加载字体
- 动态渐变背景
