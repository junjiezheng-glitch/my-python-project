# 使用 GitHub Actions 实现自动化测试

本项目实现加法和乘法，并使用 pytest 验证结果。每次推送代码或创建拉取请求时，GitHub Actions 都会在 Ubuntu 上使用 Python 3.11 自动安装依赖并运行测试。

## 项目结构

```text
my-python-project/
├── .github/workflows/ci.yml
├── calculator.py
├── test_calculator.py
├── requirements.txt
├── .gitignore
└── README.md
```

## 本地运行

```bash
python -m pip install -r requirements.txt
python -m pytest -v
```

两个测试函数分别覆盖加法与乘法，验证正数相加、正负数相加、正数相乘和乘以零。

## 查看自动测试结果

打开仓库的 **Actions** 页面，选择 **Python单元测试** 工作流，打开最新一次运行的 **test** 任务，在“运行测试”步骤查看日志。

工作流显示绿色对勾，且日志中两个测试均显示 `PASSED`、汇总显示 `2 passed`，表示测试通过；红色叉号和 `FAILED` 表示失败，需要根据日志定位并修复后重新推送。

## 作业提交

确保仓库为公开仓库，且最新一次工作流运行成功，然后将仓库首页链接提交到头歌平台。若平台还要求账号与个人访问令牌，账号填写仓库所属的 GitHub 用户名；令牌仅在平台要求的位置填写，不应提交到仓库。
