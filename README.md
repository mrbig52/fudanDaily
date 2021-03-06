# 平安复旦自动打卡

使用GitHub Actions实现全自动打卡。

## 如何使用
1. Fork 本代码库
2. 配置 Secret  
   在 Settings - Secret 页面添加如下内容：
   - USERNAME: 学号
   - PASSWORD: UIS密码
   - PUSH_KEY[可选]: Server酱SCKEY，用于推送通知，详见[http://sc.ftqq.com/](http://sc.ftqq.com/)，建议开启，可以通过微信接收打卡状态。
3. 修改[work.yml](./.github/workflow/work.yml)中的`schedule`为你喜欢的打卡时间(UTC)。真正运行会有延迟，我的情况是在延迟3分钟以内，但是 [@jiangzhouwang](https://github.com/jiangzhouwang) 同学反映延迟有15分钟，请配合Server酱通知使用。
4. 开启 Workflow  
   在 Actions 页面：
   - 开启 Workflows
   - 选择 `Fudan Daily` workflow, enable workflow

## 说明
打卡时使用前一日地理位置信息，如位置变更请提前停止自动打卡，到新位置手动打卡一次再开启。  
未经充分测试，不保证最终效果，请酌情使用。
