# OA management system
OA 管理系统
# OA管理系统项目
## 项目说明

- **三方UI库地址：**https://ant.design/index-cn

- **umi文档地址：**https://umijs.org/zh-CN

- **dva文档地址：**https://dvajs.com/guide/concepts.html#action

- **数据处理**

    > 该项目为前后端分离工程，所有涉及到数据内容均在本地数据库`mongdb`内进行获取

    

## 项目包含内容

### 业务处理

1. **登录架构设计**

    > - 接口模块封装方案
    > - 请求动作封装方案
    > - token处理方案
    > - 登录鉴权方案

2. **layout架构**

    > - 主动登出方案
    > - 被动登出方案
    > - 动态路由表处理方案
    > - 动态菜单处理方案
    > - 联动处理
    > - loading效果设计

3. **数据注入导出**

    > - 图片文件上传处理方案
    > - 前端流数据处理方案
    > - 图形化数据解析渲染

4. **权限分控**

    > - 权限处理
    > - 动态权限获取
    > - 页面权限处理方案
    > - 功能权限处理方案

5. **表格处理**

    > - 动态表格处理方案
    > - 排序及分页表格处理

6. **优化部署**

    > - 打包优化处理方案
    > - 前端项目部署方案

    

    ### 技术栈

    - **核心技术栈  reactJS （主框架）**
    - **工程构建+ 路由处理 UMIJS（reactJS工具集锦）**  
    - **状态管理 DVA** 
    - **异步数据处理 fetch**
    - **三方插件echartJS,antdesign**

---

## 项目结构功能简介



### 用户登录模块

> #### 实现管理员及员工登录功能
>
> - **账号登录**
>     - 账号密码实现登录功能
> - **手机登录**    
>     - 手机号验证码实现登录功能



> #### 密码忘记找回功能
>
>   已经注册用户（员工）可实现通过手机号码进行密码找回功能

---



### 员工分析模块

> #### 实现公司数据的可视化（图形化）展示
>
> - **员工人数分析展示**
>     - 公司总人数
>     - 在职人员工龄统计
> - **员工基本信息分析情况展示**
>     - 学历
>     - 婚姻
>     - 性别
>     - 年龄
> - **公司部门情况展示**
>     - 部门员工数量

---



### 出勤统计分析模块

> #### 当前员工出勤意外情况（迟到、早退）录入情况展示
>
> - **柱状图展示**
>     - 迟到人员数据数量统计
>     - 早退人员数量统计
> - **表格展示**
>     - 迟到人员基本信息
>     - 早退人员基本信息

---



### 员工管理模块

> #### 公司员工信息管理实现
>
> - **员工基本信息表格展示**
>     - 展示信息分为两种情况，`普通员工`展示部分信息内容，`超级管理员`可查看用户所有信息
>     - 员工信息的分页获取
>     - 根据多字段搜索条件集合实现员工查询功能
>     - 实现员工的其他相关表格本组件内部展示
> - **员工信息修改**
>     - 员工表格内实现员工信息部分字段修改
>     - 员工详情内实现员工信息部分字段修改
> - **新增员工**
>     - 实现员工基本信息的收集并保存到后端服务器
> - **员工详情**
>     - 获取当前选中员工详细信息展示
>     - 实现当前指定展示的员工信息修改
>     - 实现当前展示详情的员工删除操作
> - **员工信息删除**
>     - 删除指定员工
>     - 批量删除多个员工
>
> - **头像上传功能**
>     - 实现员工头像的单文件上传功能



---

### 部门管理模块

> #### 公司部门信息管理实现
>
> - **树状图形式展示公司所有部门基本组织架构**
>     - 上级部门信息展示
>     - 子集部门信息展示
> - **部门信息修改**
>     - 对当前选定部门内容进行指定字段修改操作
> - **新增部门**
>     - 收集新增部门信息内容并保存到后端服务器
> - **部门详情**
>     - 查看当前部门详细信息及部门关联员工数据
> - **部门删除**
>     - 删除指定的当前选中的部门
>     - 解除子部门的关联
>     - 解除父级部门关联

---

### 职级管理模块

> #### 实现员工的职级信息管理
>
> - **表格形式展示职级列表**
>     - 职级的基本信息展示
>     - 职级信息的分页展示
>     - 根据指定的职级名称进行搜索操作
> - **职级信息修改**
>     - 点击指定职级列表项可进行职级的指定字段修改操作
> - **新增职级**
>     - 设置职级字段，添加指定的职级信息
> - **职级详情**
>     - 查看当前职级详细信息
>     - 可进行当前职级的修改操作
>     - 可进行当前职级的删除操作
> - **职级删除**
>     - 删除指定的职级集合
>     - 同时删除对应的本职级内的员工的职级信息

---

### 绩效考核模块

> #### 实现员工绩效考核信息管理
>
> - **表格形式展示绩效考核记录**
>     - 员工考核记录的基本信息展示
>     - 考核记录信息的分页展示
>     - 根据员工姓名进行考核记录搜索操作
> - **考核信息修改**
>     - 点击指定考核记录项可进行指定字段修改操作
> - **新增考核记录**
>     - 新增指定员工的考核记录
> - **考核记录详情**
>     - 查看指定考核记录的详细信息
>     - 实现当前考核记录的修改操作
>     - 可进行当前考核集合的删除操作
> - **考核记录删除**
>     - 删除指定的考核记录

---

### 调薪记录模块

> #### 实现员工调薪记录信息管理
>
> - **表格形式展示员工的调薪记录**
>     - 调薪记录的基本信息展示
>     - 调薪记录信息的分页展示
>     - 根据员工姓名进行调薪记录搜索操作
> - **调薪信息修改**
>     - 点击指定调薪记录项可进行指定字段修改操作
> - **新增调薪记录**
>     - 新增指定员工的调薪记录
> - **调薪记录详情**
>     - 查看指定调薪记录的详细信息
>     - 实现当前调薪记录的修改操作
>     - 可进行当前调薪集合的删除操作
> - **调薪记录删除**
>     - 删除指定的调薪记录

---



### 奖惩记录模块

> #### 实现员工奖惩记录信息管理
>
> - **表格形式展示员工的奖惩记录**
>     - 奖惩记录的基本信息展示
>     - 奖惩记录信息的分页展示
>     - 根据员工姓名进行奖惩记录搜索操作
> - **奖惩信息修改**
>     - 点击指定奖惩记录项可进行指定字段修改操作
> - **新增奖惩记录**
>     - 新增指定员工的奖惩记录
> - **奖惩记录详情**
>     - 查看指定奖惩记录的详细信息
>     - 实现当前奖惩记录的修改操作
>     - 可进行当前奖惩集合的删除操作
> - **奖惩记录删除**
>     - 删除指定的奖惩记录

---



### 考勤记录模块

> #### 实现员工考勤记录信息管理（crud）
>
> - **表格形式展示员工的考勤记录**
>     - 考勤记录的基本信息展示
>     - 考勤记录信息的分页展示
>     - 根据员工姓名进行考勤记录搜索操作
> - **考勤信息修改**
>     - 点击指定考勤记录项可进行指定字段修改操作
> - **新增考勤记录**
>     - 新增指定员工的考勤记录
> - **考勤记录详情**
>     - 查看指定考勤记录的详细信息
>     - 实现当前考勤记录的修改操作
>     - 可进行当前考勤集合的删除操作
> - **考勤记录删除**
>     - 删除指定的考勤记录



## 项目整体实现流程

> 1. 项目基本结构搭建
> 2. 后端接口`API`公共请求方法封装处理
> 3. 公共组件制作
> 4. 公共`hook`定义
> 5. 完成各模块功能的组件化开发
> 6. 工程打包分析及构建过程
