# DeepSeek Image Generator 项目文档

## 一、项目概述

### 1.1 基本信息
- 项目名称：DeepSeek Image Generator
- 域名：deepseek-imagegenerator.com
- 技术栈：Next.js 14 + Tailwind CSS + Redis
- 部署平台：Vercel

### 1.2 核心功能
- AI图片生成
- 多语言支持（5种语言）
- IP使用限制（每IP每天3次）
- 示例展示（6个精选案例）

## 二、版本规划

### 2.1 初始版本 (v1.0)

#### 功能特性
1. **基础功能**
   - 图片生成（基于DeepSeek API）
   - IP限制（Redis实现）
   - 多语言支持
   - 示例展示

2. **页面结构**
   ```
   - Header（Logo + 语言切换）
   - 生成器区域（输入框 + 生成按钮 + 结果展示）
   - 示例展示（6个案例）
   - Footer（项目信息）
   ```

3. **技术实现**
   - 使用 Next.js 14
   - Tailwind CSS 样式
   - Redis 存储限制信息
   - Vercel 部署

### 2.2 后续迭代计划

#### v1.1 优化版本
- 图片下载功能
- 生成历史记录
- 性能优化
- 更多错误处理

#### v1.2 功能扩展版本
- 用户系统
- 收藏功能
- 分享功能
- 更多语言支持

#### v2.0 商业版本
- 会员系统
- 高级参数设置
- API接口
- 批量生成

## 三、技术细节

### 3.1 API配置
```
# API配置
API_URL=https://api.siliconflow.cn/images/generations
```

### 3.2 多语言支持
- 简体中文 (zh-CN)
- English (en)
- 日本語 (ja)
- 한국어 (ko)
- Español (es)

### 3.3 使用限制
- 每IP每天3次
- 使用Redis记录
- 24小时自动重置

### 3.4 示例展示
- 存储位置：项目内
- 更新方式：不定期手动更新
- 包含多语言提示词

## 四、设计规范

### 4.1 配色方案
```
--primary-500: #0066ff;  /* 主色调 */
--primary-600: #0052cc;  /* 深色调 */
--neutral-50:  #f9fafb;  /* 背景色 */
--neutral-700: #374151;  /* 文字色 */
```

### 4.2 响应式断点
```
--screen-sm: 640px;   /* 手机 */
--screen-md: 768px;   /* 平板 */
--screen-lg: 1024px;  /* 桌面 */
```

## 五、部署信息

### 5.1 必要服务
- Vercel（网站部署）
- Redis（使用限制）
- DNS配置（域名）

### 5.2 环境变量
```
# Redis配置
REDIS_URL=your_redis_url
REDIS_ENDPOINT=equal-katydid-10332.upstash.io
REDIS_PORT=6379
REDIS_PASSWORD=your_redis_password
REDIS_TLS=true          # 需要启用 TLS 安全连接

# API配置
API_KEY=your_api_key
API_URL=https://api.siliconflow.cn/images/generations
```

### 5.3 基础信息配置
```
# Logo配置
NEXT_PUBLIC_LOGO_URL="/images/logo.svg"
NEXT_PUBLIC_LOGO_ALT="DeepSeek Image Generator"
NEXT_PUBLIC_LOGO_WIDTH="180"
NEXT_PUBLIC_LOGO_HEIGHT="60"

# 联系信息
NEXT_PUBLIC_CONTACT_EMAIL=1731811057@qq.com

# 版权信息
NEXT_PUBLIC_COPYRIGHT_TEXT="© 2024 DeepSeek Image Generator. All rights reserved."
```

### 5.4 示例配置
```json
{
  "examples": [
    {
      "id": "1",
      "image": "/examples/images/landscape.jpg",
      "prompts": {
        "zh-CN": "日落时分的富士山，樱花飘落，远处有传统日式建筑",
        "en": "Mount Fuji at sunset with falling cherry blossoms",
        "ja": "夕暮れ時の富士山、舞い散る桜",
        "ko": "석양의 후지산, 떨어지는 벚꽃",
        "es": "Monte Fuji al atardecer con pétalos de cerezo"
      }
    }
  ]
}
```

## 六、维护说明

### 6.1 示例更新
1. 准备新的示例图片
2. 放入 public/examples/images/
3. 更新 data.json
4. 提交代码

### 6.2 错误处理
- API调用错误
- 使用限制提示
- 网络错误
- 系统错误

## 七、注意事项

### 7.1 安全性
- API密钥保护
- 请求限制
- 错误日志

### 7.2 性能
- 图片懒加载
- 请求防抖
- 浏览器缓存

### 7.3 用户体验
- 友好的加载状态
- 清晰的错误提示
- 响应式适配

## 八、更新日志

### v1.0.0 (计划中)
- 初始版本发布
- 基础功能实现
- 5种语言支持
- 示例展示