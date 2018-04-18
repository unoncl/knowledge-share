<!-- TOC -->

- [概要](#概要)
- [1. 利用空白模板创建新的应用](#1-利用空白模板创建新的应用)
- [2. App Make – 创建表单](#2-app-make--创建表单)
- [3. App Maker – 配置工作流](#3-app-maker--配置工作流)
- [4. APP Maker – 查询设计](#4-app-maker--查询设计)
- [5. App Maker –发布表单](#5-app-maker-发布表单)
- [6. App Maker – 美化首页](#6-app-maker--美化首页)
- [7. APP Maker – 配置菜单](#7-app-maker--配置菜单)
- [8. App Maker – 角色权限管理](#8-app-maker--角色权限管理)
- [9. APP Maker –系统设置](#9-app-maker-系统设置)
- [10. 配置搜索](#10-配置搜索)

<!-- /TOC -->
## 概要 ##
>本应用指南以员工入职系统为例，详细描述了如何在ExceedNotes中创建网页端应用。
>### 目标 ###
>1. 创建自己的网页端或移动端应用，及该应用端所包含的工作流程和搜索。
>2. 转换Lotus Notes应用为网页端或移动端应用。
>### 先决条件 ###
>* ExceedNotes的有效账户
>* 为该账户分配App Manager角色
## 1. 利用空白模板创建新的应用 ##
>**目标**
>
>应用ExceedNotes的空白模板创建自己的员工入职应用
>### 1.1 利用模板创建新的应用 ###
>1. 点击页面右上角的菜单键，再点击application图标。
>2. 点击Blank Template来创建新的application。
>### 1.2 填写表单并为应用生成唯一app code ###
>1. 为新建的application填写详细信息, 点击Submit完成
>    - Application Name是您要显示的名称
>    - Application Code是应用程序创建的唯一ID
>    - 在Description中可以添加关于当前应用的描述 
>    - Internal/External为确定当前程序放置在防火墙内部或外部的选项
>2. 点击 Confirm 为新的应用创建Data Source
>3. Data Source 将会被自动创建并进行初始化
>4. 系统将会展示应用详情
>5. 选择为当前的应用上传图片
## 2. App Make – 创建表单 ##
>**目标**
>
>根据具体的业务需求完成表单设计
>### 2.1 新建表单 ###
>1. 打开管理员页面， 在App Design下点击”Select”，然后选择”Form Design”
>2. 点击Add Form来创建新的表单，在输入完信息后点击Save保存设置
>    - Form name为表单的简短描述
>    - Alias name为表单的唯一ID
>    - Entity name为Mongo集合名称，建议将它设置为与Alias name相同
>    - Connection name是上一模块中创建的数据源的名称
>### 2.2 利用拖放不同类型控件完成表单设计 ###
>1. 点击Design来打开新的表单设计页面
>
>    |Tag          |Function          |
>    |-------------|:-----------------| 
>    |Design       |可视化设计界面     |
>    |Styles       |配置布局          |
>    |Javascripts  |应用地址化        |
>    |CSS          |美化表单          |
>    |Advanced     |高级功能          |
>
>2. 从左侧Toolbox菜单选择想要添加的插件，并拖放到设计面板
>3. 根据列表添加section(section是布局控件，用来控制页面里其他控件的布局)
>4. 用户可以根据需要创建所需数量的section
>5. 将左侧菜单中的控件拖放到表单中适当的位置
>    - Field 对应MongoDB中的字段名称
>    - Field Label为表单中的标签
>    - Field Control Type为在左侧菜单中可用的控件
>    - 数据类型包括：String, Int, and Float
>    - 选择Required将选项设置成必填项
>6. 根据需求继续添加sections / fields
>### 2.3 预览表单 ###
>* 在完成表单UI设计后，点击Preview来预览页面的UI设计
>### 2.4 App定制化设计 ###
>* 用户可以利用Javascripts,或点击Advanced来进行定制化设计
>    #### 2.4.1 背景图片 ####
>    1. 打开管理员页面, 在App Design中点击Select, 选择Landing Page
>    2. 在 Resource File 下点击 Add来上传背景图片
>    3. 点击 Copy Url
>    4. 在目标表单下打开 CSS，并在文本框中编辑相应代码
>    5. 替换URL地址
>    #### 2.4.2 Section边界 ####
>    * 在目标表单的CSS标签中编辑相应代码
>    #### 2.4.3 People Picker展示用户姓名 ####
>    1. 打开Form Design, 点击Add后选择添加TextBox(Hidden)
>    2. 编辑 Field
>    3. 点击展开 Advanced，并编辑 Field Value Format
>    4. 在People Picker的OnChange项目中编辑相应文本， 并点击Confirm
>    5. 刷新视图
>    #### 2.4.4 进度条 ####
>    1. 在App Design的界面下选择进入Form Design
>    2. 在CSS标签中编辑相应代码
>    3. 在Javascripts标签中编辑相应代码
>    #### 2.4.5 创建 Query ####
>    1. 在如下界面中点击Add Query
>    2. 设置或编辑相关内容
## 3. App Maker – 配置工作流 ##
>**目标**
>
>为你的项目的业务需求设计一个业务流程
>### 3.1 工作流介绍 ###
>工作流解决的主要问题是：为了实现某个业务目标，在多个参与者之间按某种预定规则自动传递表单、信息或者任务，以达到提高工作效率、更好的控制过程、有效管理业务流程等目的。
>
>ExceedNotes中的工作流引擎目前主要具有以下特性：
>- 支持通过图形拖拽方式创建和编辑Workflow
>- 支持通过表格方式创建和编辑Workflow
>- 支持业务状态的流转：向前或后退流转
>- 支持IF判断（网关）：根据实际参数不同走向不同的分支
>- 支持多人审批（会签）
>- 支持Email的灵活配置
>### 3.2 工作流组件和功能介绍 ###
>在工作流设计界面中，默认以Diagram方式打开，各个组件和功能如下所示：
>
>|名称      |描述                                                             |
>|:--------|:----------------------------------------------------------------|
>|Diagram  |以拖拽和可视化方式编辑工作流，为工作流的默认编辑方式，优点为直观和方便.|
>|Table    |以表格方式展现工作流所包含的各个元素，尤其当工作流包含的State或IF组件过多时，可通过搜索快速定位到需要修改的目标，方便快速查找定位.|
>|Connector|用于连接流程中各组件，描述流程的走向，系统会根据起始组件的类型，自动生成粗线（Event）或细线（Line）.|
>|State    |描述业务流程的各个中间状态。当业务流程流转到此状态的时候，流程会停留在此状态，直到流程对应的事件被触发，流程会流转到下一个状态.|
>|IF       |用于影响和判断流程的走向，当流程需要根据表单中某个字段值来决定走向的时候，需要添加该组件.|
>|End     |描述业务流程的终结状态，当业务流程流转到此状态的时候，流程终结，不再响应事件的流转.|
>|Save    |保存流程的设计.|
>|Action  |用于触发事件，每个Action对应于表单中相应的Button（按钮）.|
>|Argument|用于传递工作流执行所需要的数据，从而影响流程的路径或任务的分配，每个Argument对应表单中的Filed（字段）.|
>|Evenet  |Event用于响应用户的按钮操作。 当它被触发时，工作流会按照Event 的指向路径，流转到下一个状态.|
>### 3.3 配置工作流的步骤顺序 ###
>1. 在Form中启用Workflow
>2. 在Form中添加Workflow所需要的Button
>3. 在Workflow中添加Action
>4. 在Workflow中添加Argument
>5. 在Workflow中新建和配置Workflow的State（状态）
>6. 在Workflow中新建和配置Workflow的End（终结状态）
>7. 在Workflow中新建和配置IF（条件）
>8. 在Workflow中用Connector连接各组件 
>9. 在Workflow中配置生成的Event属性
>    #### 3.3.1 启用Workflow ####
>    * 通过下面路径来启用工作流: App Maker/Admin->Form Design->Edit, 在Workflow下拉列表中选择Enable.
>    #### 3.3.2 在Form中添加Workflow所需要的Button ####
>    1. 前往Form Design->Advanced界面，点击Add Button
>    2. 填写Label名称，并将Button Type设置为Workflow
>    3. 点击Confirm保存设置
>    #### 3.3.3 在Workflow中添加Action ####
>    1. 进入App Maker->Admin页面, 选择如下路径App Design->Form Design->Design
>    2. 点击Work Flow打开工作流编辑器
>    3. 点击Action->New创建一个新的Action
>    4. 在Action Name的下拉菜单中选择已创建的Action名称
>    5. 在Action Type中选择相应的类型(Forward, Backward, ToEnd)
>    6. 点击Save保存设置
>    #### 3.3.4 添加 Argument（参数） ####
>    Argument（参数）用于传递工作流执行所需要的数据，从而影响流程的路径或任务的分配。每个Argument对应表单中的一个Field（字段）。
>    1. 进入App Maker->Admin页面, 选择如下路径App Design->Form Design->Design
>    2. 点击Work Flow打开工作流编辑器
>    3. 点击Argument->New创建一个新的Argument（参数）
>    4. 选择之前在表单中创建的字段作为参数名称，同时系统将自动生成参数的类型
>    5. 点击Save保存设置
>    #### 3.3.5 添加工作流的 State（状态） ####
>    * 当工作流刚创建的时候，系统会默认生成如下两个状态Start（开始），End（结束）。每个工作流只能有1个Start状态，Start不能删除和修改，每个工作流可以有1个或多个End状态，可以修改和删除。
>    * State用于描述流程的中间状态。在State里可以设置当前状态下的页面访问权限、任务分配规则、通过规则和邮件等。
>    * 将左侧菜单中的State图标拖放到编辑器中，系统会自动默认设置名字为State + sequence number，双击进行编辑。
>    * State(状态)界面中各属性的定义
>
>    |参数                |定义
>    |:-------------------|:-------------------------------------------------------|
>    |State Name（状态名称）|在工作流和表单中显示的名称|
>    |State Code（状态代码）|状态的唯一标识，在同一个工作流中不能重复|
>    |Is End State（是否结束状态）|如果为“End（结束）” ，系统将更新工作流的状态为结束|
>    |Enable Edit Mode（启用编辑模式）|如果选中，则在这个状态下可以进行文档的编辑操作|
>    |Visit Mode（显示模式）|控制表单在该状态下对外公开模式，Public ：有表单访问权限的人都能访问，Private: 当前状态的相关的人员才能访问|
>    |Assignment Type（分配类型）|此状态下的任务分配类型.  包括3种类型： BySubmitter， FromArgument，Role|
>    |Assignment Value（分配类型的值）|如果为“BySubmitter”, 这个值默认为BySubmitter（提交人）；如果为“FromArgument”, 这个数据源为 类型为“User（用户）” 的Argument （参数）；如果为 “Role”, 这个数据源为所有的Role（角色），可在“Roles Management”中定义Role（角色）|
>    |Pass Rule（通过规则）|如果选择“All”，当所有的审批者都同意后，才会跳转到下一个状态; 如果为“Any”，任意审批者操作后，即可跳转到下一个状态|
>    |Bind Event（绑定事件）|当“Pass Rule” 为“All”时才会显示, 需要选择一个Event（事件）作为所有审批者的操作|
>    #### 3.3.6 添加工作流的 End（终结状态） ####
>    * End状态为工作流的结束状态,当流程流转到此状态的时候，流程结束，每个流程可以有多个End（终结状态）。
>    * End与State的主要区别为：End状态下不需要设置Assignment（任务分配）等属性。在工作流编辑器中，双击或拖入新End状态（如果流程需要多个终结状态），然后双击进行编辑。 
>    #### 3.3.7 新建和配置IF（条件） ####
>    * IF（判断条件）根据判断条件和参数值决定工作流会流转到哪个状态，它必须提前创建好至少一个Argument（参数）作为判断的条件。
>    * 在工作流编辑器中拖入IF, 然后双击进行编辑。
>    * 在弹出的编辑页面，点击+，在弹出框中设置参数和条件，然后点击Save保存设置。
>    #### 3.3.8 用Connector连接各组件 ####
>    * Connector（连接线）用于连接流程中各组件元素，并显示流程的流转方向。系统会根据起始组件元素的类型，自动生成粗线（Event）或细线（Line）。
>    * 如果连线中起始组件的类型为State，生成粗线对应为Event（事件），需要点击以配置相应的属性。
>    * 如果连线中起始组件的类型为IF, 生成细线对应为Line（连线），并自动生成连线的名称Yes和No，不需要编辑。
>    1. 在左侧的菜单面板中点击Connector, 然后在编辑区域中先后点击2个需要连接的组件元素，系统将自动生成连接线，及连接线名称。
>    2. 按照流程的实际需要，依次点击Connector并连接编辑区域中各组件元素，然后拖动元素的位置以完成组件的布局。
>    #### 3.3.9 配置生成的Event属性 ####
>    + 连接线创建好以后，双击各个粗线对应的Event（事件）进行Property属性的编辑。
>    + Form和To 标签栏是作为描述连接线的起初和结束的元素，不需要配置。
>    + 各个连接线的属性配置完成以后，示例如下图所示。至此步骤，除了邮件部分，一个流程已经配置完成。 
>### 3.4 配置流程中的邮件功能 ###
>1. 在流程编辑区域中，双击需要添加邮件的元素，在弹出的界面中，点击+Email List 配置相应的属性。
>    * 界面中各属性描述如下
>
>    |属性名称        |描述                                                       |
>    |:--------------|:----------------------------------------------------------|
>    |Email Name|邮件名称|
>    |Template List|在System Setting中配置的邮件模板列表，需要选择1个模板，然后根据模板的内容和参数，进行相应的参数设置|
>    |From（发件人）, To（收件人）CC(抄送人），Reply（回复人）|第一个下拉框为参数类别选择，第二个下拉框为参数类别对应的可选择的值。第一个下拉框有三个可选择的值：FromArguments，FromConstants和SystemVariable。|
>    |Subject（邮件标题）|在Template（邮件模板）里配置，此处只显示不可编辑|
>    |Content（邮件内容）|在Template（邮件模板）里配置，此处只显示不可编辑|
>    |Parameters（邮件参数）|来源于邮件版本中对Subject和 Content里的参数设置，第一个下拉框为参数类别选择，第二个下拉框为参数类别对应的可选择的值，第一个下拉框有三个可选择的值：FromArguments，FromConstants和SystemVariable。|
>2. 在Parmeters（参数）中设置相关信息。
>3. 点击Save保存邮件配置。
>4. 点击OK保存Event（事件）配置 ，完成邮件配置。
## 4. APP Maker – 查询设计 ##
>**目标**
>
>利用过滤器和分组进行应用的查询设计
>### 4.1 新建查询 ###
>1. 打开管理员页面， 在App Design下选择Form Design
>2. 在Form Design界面，点击Design对相应的表单进行编辑
>3. 点击Query, 再点击Add Query以创建新的查询（Query）
>### 4.2 配置查询过滤器和查询分组 ###
>1. 配置查询过滤器(Query Filter)和查询分组(Query Grouping)
>2. 点击Save changes保存设置
## 5. App Maker –发布表单 ##
>**目标**
>
>理解如何管理并控制表单的版本
>### 5.1 发布表单 ###
>1. 打开管理员页面，在App Design下选择Form Design
>2. 在相应的表单记录上点击Design打开表单
>3. 点击Build打开发布面板
>4. 查看之前的操作
>5. 在页面底部点击Build
>6. 输入版本信息并选择部署环境
>7. 点击Confirm发布当前的版本
>### 5.2 版本管理 ###
>1. 打开管理员页面，在App Design下选择打开Form Design
>2. 点击Version显示当前表单的所有版本
>3. 点击Set environment来发布该版本到相应的环境
>4. 勾选Production，再点击Confirm来发布最新版本到生产环境
## 6. App Maker – 美化首页 ##
>**目标**
>
>美化首页
>### 6.1 为首页上传源文件 ###
>1. 打开管理员页面，在App Design下选择点击Landing Page
>2. 点击进入Resource File页面
>3. 点击Add上传图片
>### 6.2 编写首页HTML和CSS ###
>1. 打开管理员页面，在App Design下选择点击Landing Page
>2. 进入Landing Page界面，并在HTML编辑器中编辑相关代码或者更新图片
>3. 点击Preview按钮查看结果
>4. 点击Save按钮完成登录页的编辑
## 7. APP Maker – 配置菜单 ##
>**目标**
>
>理解并掌握如何管理应用菜单及其功能
>1. 打开管理员页面，在App Design中选择点击App Function
>2. 右键点击已创建的Application Name，并在菜单中选择需要添加的组件
>3. 在App Function弹出框中，输入组件名称，点击Save保存设置
>4. 在右侧Information界面编辑新添加组件的相关信息，点击Save保存设置
## 8. App Maker – 角色权限管理 ##
>**目标**
>
>理解并掌握角色权限管理
>### 8.1 管理角色 ###
>1. 打开管理员页面, 在App Design下选择点击Role Management
>2. 点击Manage打开角色管理面板
>3. 系统提供了5种角色可供选择，如下表所示
>
>    |Default role    |Description          |
>    |:---------------|:--------------------|
>    |AppAdmin|应用的管理员，来管理该应用|
>    |AppDesign|设计应用，如表单，查询，权限控制，以及二次开发等|
>    |Author|文档作者，编辑自己创建的文档|
>    |Editor|编辑有权限的文档|
>    |Reader|只读有权限的文档|
>4. 选定了角色后，选择User或Group来授予或移除用户或用户组权限
>5. 点击Add或Remove授予或解除选定用户或用户组的权限
>6. 点击Confirm保存设置
>### 8.2 创建新角色 ###
>1. 打开角色管理面板，点击Add添加新的角色
>2. 输入角色名称，点击Save确认保存
## 9. APP Maker –系统设置 ##
>**目标**
>
>配置应用的下拉菜单和设置
>### 9.1 控件数据源（列表） ###
>1. 打开管理员页面，在System Settings下选择点击List
>2. 点击右手边的菜单中的Add来管理列表
>3. 点击 Add以增加列表项目
>4. 输入列表信息并点击Accept
>5. 选择右侧的列表名称，可页面左侧对其信息进行修改
>### 9.2 设置 ###
>1. 打开管理员页面，在System Settings下选择点击Settings
>2. 启用搜索设置
>3. 根据需求选择应用级别的全局格式
>4. 在DateTime Format Settings下选择相应的时间显示模式，点击Save保存设置
>5. 在Skin Selection下选择应用界面：Ocean Blue或者PwC Light，点击Save保存设置
>6. 在Application Name下修改应用名称
>7. 在Application Logo下修改应用图标
>### 9.3 邮件模板 ###
>1. 打开管理员页面，在System Settings下选择点击Email Template
>2. 选择进入Email Parameter界面, 点击Add来添加新的参数
>3. 在弹出框中添加相应信息，点击Submit保存设置 
>4. 选择进入Email Template界面，点击Add添加新的邮件模板
>5. 在弹出框中添加相应信息，点击Submit保存设置
## 10. 配置搜索 ##
>**目标**
>
>配置并启用搜索功能
>### 10.1 新建索引 ###
>1. 在管理页面中点击菜单图标, 并选择ADVANCED SEARCH
>2. 点击Manage Index
>3. 在右上角点击+按钮来添加索引并进入新的索引配置页
>4. 在弹出框中选择索引类型
>5. 为索引选择data source
>6. 进入BASIC界面，选择Date Collection，并修改Index Name（索引名称为大小写敏感）
>7. 进入SETTING界面，对Analysis保持原默认设定
>8. 进入MAPPINGS界面，点击右上角图标，选择需要被查找的字段，点击SAVE保存
>9. 进入STATUS界面可以查看数据状态
>### 10.2 新建别名 ###
>* 在左侧菜单中点击Manage Alias，进入Alias Management页面。输入Alias Name，并查看索引和过滤条件。
>### 10.3 配置搜索 ###
>1. 在左侧菜单中点击Search Configuration，进入Search Configuration页面
>2. 选择想要搜索的索引，根据需要对其设置进行更改，最后保存
>### 10.4 搜索预览 ###
>1. 在左侧菜单中点击Search Preview按钮，进入Search Preview页面。点击右上角的刷新按钮来刷新Search Code。
>2. 选择Search Code，并在Criteria中填写查询条件，点击Search进行查询，同时验证之前搜索的相关配置是否成功。
>### 10.5 启用搜索 ###
>1. 进入Application页面，在Search Application中输入搜索条件，并进行搜索。
>2. 进入搜索到的应用,  点击Admin， 在System Settings中选择Settings。
>3. 在Enable Search中选择Yes启用搜索。在Search Selection和Search code设置相应的搜索，点击Save启用搜索。
>4. 搜索条将会显示在页面顶端。输入查询关键词，点击Enter后搜索结果将会被列在页面中。
>### 10.6 更新主页的搜索框设置 ###
>1. 进入管理员页面，在App Design下选择Landing Page
>2. 进入Landing Page界面
>3. 修改首页上的按钮对应的链接

































    
