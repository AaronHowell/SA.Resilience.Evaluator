SA.Resilience.Evaluator is a tool automatically evaluate resilience of software architecture.

Architecture resolver:
| File name          | Code type | Lines of code | Function                                                  |
| ------------------ | --------- | ------------- | ---------------------------------------------------------- |
| CPP_Parsing.cpp    | C++       | 2371          | Analysis of basic code information and calling relationships |
| DDAnalysis.cpp     | C++       | 744           | Data dependency analysis                                   |
| CodeInfoExtract.py | Python    | 1683          | Basic information processing of code                       |
| BuildCG.py         | Python    | 651           | Graph construction                                         |
| process_cfg.py     | Python    | 1120          | CFG construction                                           |
| cdg.py             | Python    | 166           | CDG construction                                           |
| ddg.py             | Python    | 570           | DDG construction                                           |
| sdg.py             | Python    | 748           | SDG construction                                           |
| pipe_filter.py     | Python    | 248           | ADG construction   

Attack surface analyzer:
<img width="875" height="504" alt="图片1" src="https://github.com/user-attachments/assets/dfcfd137-615f-41f4-92ac-0941bcc2d227" />

Resilience evaluation component:
| Data                  | Type    | Description                                                  |
| --------------------- | ------- | ------------------------------------------------------------ |
| attack_set_chart_data | List    | Pie chart data for the attack surface information interface  |
| entry_exit_points_num | Integer | Sum of entry and exit nodes on the attack surface            |
| untrusted_data_item_nums | Integer | Number of untrusted data elements in the attack surface      |
| data_channel_num      | Integer | Number of data channels in the attack surface                |
| attacks_category_info_table | List | List of potential attack types and their basic information   |
| entry_exit_points_table | List    | Detailed list of the system's entry and exit nodes           |
| untrusted_data_items_table | List | Detailed list of untrusted data elements in the system       |
| attack_set_detail_table | List    | Detailed list of the system's potential attack sets          |

parameter table listing all weights and defaults:
| Parameter Name          | Symbol          | Description                                                  | Default Value | Search Range (if applicable) | Source / Notes                          |
| ----------------------- | --------------- | ------------------------------------------------------------ | ------------- | ----------------------------- | --------------------------------------- |
| Reconstruction loss weight | $\lambda_{rec}$ | Weight for the reconstruction term in the loss function       | 1.0           | [0.1, 10]                     |         |
| KL divergence weight    | $\beta$         | Controls regularization strength in the VAE                   | 0.5           | [0.01, 1.0]                   |          |
| Learning rate           | $\eta$          | Optimizer learning rate                                       | $10^{-4}$     | —                             |      |


