# GitHub与Streamlit更新步骤

1. 打开本文件所在文件夹，全选其中全部文件和子文件夹。
2. 上传到现有GitHub仓库 `weien405/sofa` 的根目录，保留目录结构。
3. 如果GitHub提示同名文件，选择替换或提交新版本。
4. 务必确认仓库出现：
   `model/XGBoost_FINAL_TRAINING_ONLY_PIPELINE.pkl`。
5. 务必确认GitHub中的入口仍为根目录下的 `app.py`。
6. 打开Streamlit Community Cloud中的现有应用，进入Manage app。
7. 确认Repository为 `weien405/sofa`，Branch为 `main`，Main file path为 `app.py`。
8. 点击Reboot app；如果没有自动读取最新提交，执行Redeploy。
9. 页面正常时应显示14项输入，而不再显示模型不可用提示。
10. 用页面的合成示例核查预测值约为 `5.109136%`。

不要上传任何患者级文件、数据库凭据或其他模型。
