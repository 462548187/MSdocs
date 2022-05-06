
### 克隆本仓库
```bash
git clone https://github.com/462548187/MSdocs.git
```

### 安装依赖
```bash
pip install -r requirements.txt
```

### 修改文档内容
本文档的文档结构定义在 `mkdocs.yml` 文件中，文档的具体内容均在 `docs` 目录中。
```yaml
..........
nav:
    - 项目介绍: index.md
    - 用户手册:
          - 通用功能: user_manual/general.md
          - 测试跟踪:
                - 模块说明: user_manual/test_track/intro.md
                - 首页: user_manual/test_track/home.md
                - 功能用例: user_manual/test_track/test_case.md
                - 用例评审: user_manual/test_track/test_case_review.md
                - 测试计划: user_manual/test_track/test_plan.md
                - 缺陷管理: user_manual/test_track/test_defect.md
                - 报告: user_manual/test_track/test_report.md
                - 用例拓展: user_manual/test_track/test_expand.md
          - 接口测试:
                - 模块说明: user_manual/api_test/intro.md
                - 首页: user_manual/api_test/home.md
                - 接口定义: user_manual/api_test/api_definition.md
                - 接口自动化: user_manual/api_test/api_automation.md
                - 接口测试报告中心: user_manual/api_test/test_report.md
                - 用例步骤说明: user_manual/api_test/api_step.md
                - 内置函数: user_manual/api_test/functions.md
          - 项目设置:
                - 项目信息: user_manual/project_management/project_info.md
                - 项目成员: user_manual/project_management/project_user.md
                - 用户组与权限: user_manual/prosject_management/usergroup_permission.md
                - 项目环境: user_manual/project_management/project_environment.md
                - 文件管理: user_manual/project_management/file_management.md
                - 自定义代码片段: user_manual/project_management/customcode_snippets.md
                - 操作日志: user_manual/project_management/operation_log.md
                - 应用管理: user_manual/project_management/application_management.md   
    -
..........
```

文档内容使用 markdown 语法编写，若要添加新的文档，需要先在 `mkdocs.yml` 文件中的 `nav` 部分增加对应章节导航。

### 本地调试文档
```bash
mkdocs serve
```
执行上述命令后，可通过 `http://127.0.0.1:8000` 地址查看生成的文档内容，当修改文档后，页面内容会自动更新。

### 构建文档
```bash
mkdocs build
```

执行上述命令后，会在 `site` 目录下生成文档站点的静态文件，将目录中的内容复制到任意 HTTP 服务器上即可完成文档的部署。
