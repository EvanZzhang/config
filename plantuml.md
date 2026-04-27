PUML 各类图表统一风格成品提示词（可直接复制）
说明：4条提示词共用同一套风格约束，保证架构图、流程图、时序图、组件图视觉统一（浅灰直角、直角连线、黑白灰极简风），同时适配各图表语法特性，避免渲染失败，直接粘贴给AI即可生成可用图。
提示词1：系统架构图 / 分层架构图（直接复制粘贴）
严格采用【国内企业项目/开源项目标准极简架构风格】：
1. 配色：纯白背景，模块浅灰色填充 #F0F0F0，深灰色边框 #808080，文字黑色
2. 形状：全部使用直角矩形，禁止圆角、禁止渐变、禁止阴影、禁止3D效果、禁止插画图标
3. 连线：全局强制正交直角连线，只允许水平/垂直折线，禁止斜线、曲线、交叉连线
4. 字体：统一使用微软雅黑，字号适中，排版整洁
5. 布局：自上而下、从左至右有序排布，模块间距均匀，杜绝重叠、杂乱
6. 输出：只输出纯标准PlantUML代码，以@startuml开头、@enduml结尾，无多余解释、无注释、无特殊简写语法
7. 语法：使用PlantUML官方稳定兼容语法，杜绝非标简写、非法箭头、冲突布局参数，保证可直接渲染成功

【架构图专属规则】
1. 采用垂直分层结构，使用package严格划分层级：接入层/网关层/业务服务层/中间件层/缓存层/数据存储层
2. 同层级模块横向均匀排列，核心业务居中，中间件、监控、辅助组件右侧独立排布
3. 依赖流向严格：从上到下、从外到内，只保留核心业务连线，删减次要弱依赖，防止连线爆炸交叉
4. 每层独立容器包裹，层级边界清晰，服务、中间件、存储分类明确
5. 禁用时序图语法，纯组件+依赖结构

同时在PUML代码开头添加以下固定样式，保证风格统一：
skinparam linetype ortho
skinparam defaultFontName "Microsoft YaHei"
skinparam defaultFontSize 11
skinparam backgroundColor #FFFFFF
skinparam lineColor #666666
skinparam rectangle {
    BackgroundColor #F0F0F0
    BorderColor #808080
    RoundCorner 0
}
提示词2：业务流程图 / 活动流程图（直接复制粘贴）
严格采用【国内企业项目/开源项目标准极简架构风格】：
1. 配色：纯白背景，模块浅灰色填充 #F0F0F0，深灰色边框 #808080，文字黑色
2. 形状：全部使用直角矩形，禁止圆角、禁止渐变、禁止阴影、禁止3D效果、禁止插画图标
3. 连线：全局强制正交直角连线，只允许水平/垂直折线，禁止斜线、曲线、交叉连线
4. 字体：统一使用微软雅黑，字号适中，排版整洁
5. 布局：自上而下、从左至右有序排布，模块间距均匀，杜绝重叠、杂乱
6. 输出：只输出纯标准PlantUML代码，以@startuml开头、@enduml结尾，无多余解释、无注释、无特殊简写语法
7. 语法：使用PlantUML官方稳定兼容语法，杜绝非标简写、非法箭头、冲突布局参数，保证可直接渲染成功

【流程图专属规则】
1. 使用标准活动图语法：start、end、if分支、partition阶段分区
2. 按业务阶段划分分区：初始化、预处理、核心处理、后置处理、收尾
3. 逻辑单向流转，分支收拢整齐，多余分支合并简化
4. 判断菱形样式统一，流程节点大小一致，上下对齐
5. 合理合并重复逻辑，不堆砌细碎步骤，保证图面清爽可读

同时在PUML代码开头添加以下固定样式，保证风格统一：
skinparam linetype ortho
skinparam defaultFontName "Microsoft YaHei"
skinparam defaultFontSize 11
skinparam backgroundColor #FFFFFF
skinparam lineColor #666666
skinparam rectangle {
    BackgroundColor #F0F0F0
    BorderColor #808080
    RoundCorner 0
}
skinparam activity {
    BackgroundColor #F0F0F0
    BorderColor #808080
}
skinparam condition {
    BackgroundColor #F9F9F9
    BorderColor #808080
}
提示词3：接口时序图 / 调用时序图（直接复制粘贴）
严格采用【国内企业项目/开源项目标准极简架构风格】：
1. 配色：纯白背景，模块浅灰色填充 #F0F0F0，深灰色边框 #808080，文字黑色
2. 形状：全部使用直角矩形，禁止圆角、禁止渐变、禁止阴影、禁止3D效果、禁止插画图标
3. 连线：全局强制正交直角连线，只允许水平/垂直折线，禁止斜线、曲线、交叉连线
4. 字体：统一使用微软雅黑，字号适中，排版整洁
5. 布局：自上而下、从左至右有序排布，模块间距均匀，杜绝重叠、杂乱
6. 输出：只输出纯标准PlantUML代码，以@startuml开头、@enduml结尾，无多余解释、无注释、无特殊简写语法
7. 语法：使用PlantUML官方稳定兼容语法，杜绝非标简写、非法箭头、冲突布局参数，保证可直接渲染成功

【时序图专属规则】
1. 严禁使用 package、层级容器等架构图语法，避免渲染失败
2. 使用 actor、participant 定义所有参与者，顺序从上至下排列
3. 消息调用单向有序，请求下行、响应上行，箭头规范统一
4. 精简冗余交互，只保留关键请求/响应/回调逻辑
5. 不添加复杂样式参数，保证时序图语法纯净、渲染稳定

同时在PUML代码开头添加以下固定样式，保证风格统一：
skinparam linetype ortho
skinparam defaultFontName "Microsoft YaHei"
skinparam defaultFontSize 11
skinparam backgroundColor #FFFFFF
skinparam lineColor #666666
skinparam actor {
    BackgroundColor #F0F0F0
    BorderColor #808080
}
skinparam participant {
    BackgroundColor #F0F0F0
    BorderColor #808080
}
提示词4：组件图 / 模块依赖图（直接复制粘贴）
严格采用【国内企业项目/开源项目标准极简架构风格】：
1. 配色：纯白背景，模块浅灰色填充 #F0F0F0，深灰色边框 #808080，文字黑色
2. 形状：全部使用直角矩形，禁止圆角、禁止渐变、禁止阴影、禁止3D效果、禁止插画图标
3. 连线：全局强制正交直角连线，只允许水平/垂直折线，禁止斜线、曲线、交叉连线
4. 字体：统一使用微软雅黑，字号适中，排版整洁
5. 布局：自上而下、从左至右有序排布，模块间距均匀，杜绝重叠、杂乱
6. 输出：只输出纯标准PlantUML代码，以@startuml开头、@enduml结尾，无多余解释、无注释、无特殊简写语法
7. 语法：使用PlantUML官方稳定兼容语法，杜绝非标简写、非法箭头、冲突布局参数，保证可直接渲染成功

【组件图专属规则】
1. 以组件、模块、第三方系统为核心单元
2. 内部服务实线、外部第三方系统虚线区分
3. 标注接口依赖、服务调用、数据交互关系
4. 关联组件就近排布，强耦合模块相邻放置
5. 整体扁平化分层，不做多层嵌套，降低连线交叉

同时在PUML代码开头添加以下固定样式，保证风格统一：
skinparam linetype ortho
skinparam defaultFontName "Microsoft YaHei"
skinparam defaultFontSize 11
skinparam backgroundColor #FFFFFF
skinparam lineColor #666666
skinparam rectangle {
    BackgroundColor #F0F0F0
    BorderColor #808080
    RoundCorner 0
}
skinparam artifact {
    BackgroundColor #F0F0F0
    BorderColor #808080
}
使用说明
- 每条提示词均包含「全局风格约束+图表专属规则+固定样式头」，无需额外修改，直接粘贴给AI（豆包、GPT、Trae等）即可。
- 所有图表生成后，风格完全统一（浅灰直角模块、直角连线、纯白背景），无割裂感，可直接用于文档、答辩、项目汇报。
- 若渲染失败，无需修改提示词，直接复制生成的PUML代码，粘贴到 https://www.planttext.com/ 即可成功渲染（最稳定兼容）。
