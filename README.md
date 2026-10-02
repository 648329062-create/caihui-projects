# 财会项目

面向财务、会计和财务自动化开发人员的开源项目清单与中文使用指南。整理日期：2026-10-02。功能依据官方仓库资料整理，尚未部署验证。

## 项目清单

| 项目 | 适用场景 | 上手门槛 | 中文使用路线 |
| --- | --- | --- | --- |
| [ERPNext](https://github.com/frappe/erpnext) | 企业总账、应收应付、采购销售与财务协同 | 高，需要部署和实施 | 先体验演示环境，再配置公司、科目与期初余额；用销售发票、采购发票和收付款测试总账及往来核对 |
| [Akaunting](https://github.com/akaunting/akaunting) | 小企业在线财务、收入支出管理 | 中，需要服务器 | 按官方说明部署，建立公司和客户供应商，录入收入支出；核对所需功能是否依赖商店扩展 |
| [Frappe Books](https://github.com/frappe/books) | 小企业离线记账、复式记账和财务报表 | 低至中，桌面应用 | 核查发布状态，创建测试账套，配置科目，录入发票、付款与日记账，查看总账、试算平衡表、利润表和资产负债表 |
| [InvoicePlane](https://github.com/InvoicePlane/InvoicePlane) | 客户、报价、商业账单与回款跟踪 | 中，需要自托管 | 建立客户和商品，创建报价及账单，登记付款，检查模板和付款状态 |
| [Beancount](https://github.com/beancount/beancount) | 文本复式记账、可审查账本、自动化导入基础 | 中，需要文本与命令行 | 使用当前稳定 v3，创建账户与交易文本文件，录入样例交易，检查余额及错误，再设计银行流水转换流程 |
| [Firefly III](https://github.com/firefly-iii/firefly-iii) | 个人收支、预算、分类和现金流观察 | 中，需要自托管 | 体验官方演示，按文档部署，建立账户、分类和预算，录入测试收支；批量导入按官方配套工具文档操作 |
| [XlsxWriter](https://github.com/jmcnamara/XlsxWriter) | 自动生成 Excel 月报、预算表、图表和管理报表 | 中，需要 Python | 安装 Python 包，从官方 examples 开始，把已核对的数据写入工作簿，添加金额格式、公式、筛选和图表，在 Excel 中核验输出 |

## 怎么开始

1. **企业会计与业务一体化**：评估 ERPNext，准备业务流程、科目、币种与期初数据，安排技术人员协助实施。
2. **小企业收支管理**：比较 Akaunting 和 Frappe Books，按在线协作或本地桌面使用需求选择。
3. **账单与回款**：试用 InvoicePlane，用虚构客户走一次报价、账单和付款流程。
4. **Excel 报表自动化**：使用 XlsxWriter，以匿名数据生成月度收入、费用与预算对比表。
5. **个人预算**：试用 Firefly III；需要文本账本与版本管理时评估 Beancount。

## 使用边界与选型检查

- 商业账单功能不代表支持中国税务发票开具；中国会计科目、税务申报、电子发票与当地规则需要逐项核实。
- Firefly III 面向个人财务，XlsxWriter 是报表开发库；分别核对用途与企业会计需求。
- Frappe Books 官方 README 当前提示代码签名证书问题阻碍新版本发布，采用前检查最新公告和 Releases。
- Akaunting 有扩展商店，逐项核实所需功能与费用，不能据开源仓库推断所有扩展免费。
- 正式迁移前，以样例数据验证币种、期间、科目、导入格式、凭证、余额和报表，保留原始数据及备份。
- 二次开发或分发前查看各项目当前 LICENSE。本仓库整理链接与使用路线，不包含上游源码。

## 官方资料

- [ERPNext 会计模块](https://github.com/frappe/erpnext/blob/develop/erpnext/accounts/README.md)
- [Akaunting 安装与要求](https://github.com/akaunting/akaunting#readme)
- [Frappe Books 功能与发布状态](https://github.com/frappe/books/blob/master/README.md)
- [InvoicePlane 官方说明](https://github.com/InvoicePlane/InvoicePlane#readme)
- [Beancount 官方说明与文档入口](https://github.com/beancount/beancount#readme)
- [Firefly III 官方说明](https://github.com/firefly-iii/firefly-iii#readme)
- [XlsxWriter 文档](https://xlsxwriter.readthedocs.io/)

后续维护优先核对官方 README、Releases、许可证和安装文档，不以 star 数作为唯一筛选标准。
