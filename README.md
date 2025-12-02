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
| Parameter name               | Symbol       | Description                          | Default value                          |Where|
|-------------------------------|--------------|--------------------------------------|----------------------------------------|---|
| Probability of attack         | Probability(Attack) | The probability of attack        | Medium: 0.5<br>High: 0.8<br>Low: 0.2<br>Uncertainty: user’s input |attack_surface_info.py|
| weights (cyclomatic complexity) | wc          | The weight of cyclomatic complexity  |  temp = c[2] + child[2]                             |Component_recovery.py|
| weights (entries)             | wp           | The weight of entries                | temp = c[2] + child[2]                                  |Component_recovery.py|
| weights (external library dependencies) | wp | The weight of external library dependencies |  temp = c[2] + child[2]                         |Component_recovery.py|
| weights (control dependency)  | wcontrol     | The weight of control dependency     | degree_dict[func] += parent[2]                                   |Component_recovery.py|
| weights (data dependency)     | wdata        | The weight of data dependency        | degree_dict[func] += parent[2]                                     |Component_recovery.py|
| weights (API dependency)      | wapi         | The weight of API dependency         | degree_dict[func] += parent[2]                                     |Component_recovery.py|
| weights (interface dependencies) | α          | The weight of interface dependencies |weight = int(temp_edge["count"])                                  |Component_recovery.py|
| weights (direct dependencies) | β            | The weight of direct dependencies    |weight = int(temp_edge["count"])                                    |Component_recovery.py|

 the UML/ADG inputs used in figures so others can reproduce the plots：\back_end\test1\wsd_uml_folder
