# Daybreak-of-Teyvat-Gamma-Version
Daybreak of Teyvat Gamma Version

https://github.com/Mung-Bean-Cake/Daybreak-of-Teyvat-Gamma-Version

模仿带有GUN的文件名的文件，为纳塔NAT国家设计对应的national_focus（含80个focus id）、event（80个）、decision（40个）、idea（30个）、localisation。故事设计应该贴合原神游戏中纳塔国家的剧情。效果代码可以参考该网站的解释【https://hoi4.paradoxwikis.com/List_of_modifiers】【https://hoi4.paradoxwikis.com/Effect】

一个单独的focus应该这样写：
focus = {
id = GUN_The_Gunnhild_Family_Meeting
icon = GFX_Goal_MOT_Balance
cost = 8.00
x = 63
y = 1
completion_reward = {
custom_effect_tooltip = GUN_Make_The_Gunnhild_Family_Meeting
add_political_power = 160
set_country_flag = GUN_The_Gunnhild_Family_Meeting
add_equipment_to_stockpile = { type = fighter_equipment_1  amount = 50 producer = MOT }
country_event = { id = Ilyich_Character.1  days = 1  }
country_event = { id = Ilyich_Weapon.1  days = 1  }
country_event = { id = GUN_Event.1  days = 15  }
}
}
效果代码可以参考该网站的解释【https://hoi4.paradoxwikis.com/Effect】

你应该修改XY坐标，使国策的布局，像树木的根系一样，从上到下展开。两个相邻国策的X坐标应该间隔2。

一个单独的event应该这样写：
country_event = {
id = GUN_develop_economy.1
title = GUN_develop_economy.1.t
desc = GUN_develop_economy.1.d
picture = GFX_GUN_Event_03
fire_only_once = yes
is_triggered_only = yes		
option = {
name = GUN_develop_economy.1.a
custom_effect_tooltip = GUN_Effects_are_Hidden
add_equipment_to_stockpile = { type = infantry_equipment  amount = 500  producer = LYY }
add_political_power = 10
}
}
效果代码可以参考该网站的解释【https://hoi4.paradoxwikis.com/Effect】


一个单独的idea应该这样写：
GUN_Family = {
picture = idea_MOT
allowed = { always = yes }
allowed_civil_war = { always = yes }
modifier = {
army_defence_factor = 0.12
army_attack_factor = 0.12
stability_factor = 0.12
}
}
idea的修正效果代码可以参考该网站的解释【https://hoi4.paradoxwikis.com/List_of_modifiers】
一个单独的decison应该这样写：
NAT_decision_01 = {
icon = eng_install_government
available = { tag = NAT	}
visible = { tag = NAT }
fire_only_once = yes
modifier = { }
ai_will_do = { factor = 1 }
cost = 50
complete_effect = {   
add_to_variable = { var = dx value = 5 }
add_ideas = NAT_Flame_Tribe_Unity
add_equipment_to_stockpile = { type = infantry_equipment  amount = 500  producer = LYY }
add_political_power = 10
}		
}

为上传的代码文件撰写localisation。
localisation的写法范例如下
LYY_Rock_and_Covenant:"岩与契约的海港"
LYY_Rock_and_Covenant_desc:"这里是璃月，在岩王帝君千年庇佑下长足发展的全提瓦特最繁华的港口，有着极为成熟的海上商路，全大陆的摩拉源源不断地涌向这里。"
localisation中desc的内容应该有200字左右，文辞优美、富有趣味、贴近纳塔故事背景。
必须完整输出，不要简单的节选。

NAT_Event.1.t:"召集部族议会"
NAT_Event.1.d:"赤红的火山熔岩映照着纳塔的大地，千百年来，散落的部族如星火般分布在这片燃烧的土地上。而今，深渊的阴影悄然蔓延，部族间的裂隙渐生，玛薇卡的火焰意志亟待凝聚。你决意召集所有部族的首领齐聚图兰圣城，在火神的注视下共商大计。是以温和的姿态倾听各部落的诉求，以火焰的包容弥合分歧，让纳塔的政治力量如熔岩般凝聚，稳固这片土地的根基；还是秉持强硬的立场，以绝对的权威划定规则，虽能强化统治，却可能让部分部族心生隔阂。每一个选择，都将牵动纳塔未来的走向，火焰的道路，从来都由抉择铸就。"
NAT_Event.1.a:"以火焰包容，共商纳塔大计"
NAT_Event.1.b:"以铁腕立规，凝聚统治权威"

为上传的【珊瑚宫（海祇岛）剧本核心介绍：深度重构与多元抉择】中的决议、理念的代码文件撰写localisation。
localisation的写法范例如下
LYY_Rock_and_Covenant:"岩与契约的海港"
LYY_Rock_and_Covenant_desc:"这里是璃月，在岩王帝君千年庇佑下长足发展的全提瓦特最繁华的港口，有着极为成熟的海上商路，全大陆的摩拉源源不断地涌向这里。"
localisation中desc的内容应该有200字左右，文辞更优美、更有趣味、贴近海祇岛故事背景。
必须完整输出，不要简单的节选。

为上传的【珊瑚宫（海祇岛）剧本核心介绍：深度重构与多元抉择】中的国策部分的代码文件撰写localisation。
localisation的写法范例如下
LYY_Rock_and_Covenant:"岩与契约的海港"
LYY_Rock_and_Covenant_desc:"这里是璃月，在岩王帝君千年庇佑下长足发展的全提瓦特最繁华的港口，有着极为成熟的海上商路，全大陆的摩拉源源不断地涌向这里。"
localisation中desc的内容应该有200字左右，文辞更优美、更有趣味、贴近海祇岛故事背景。
必须完整输出，不要简单的节选。


请你根据上传文档中对纳塔的描述，以及代码文档中对纳塔剧本的设计，对我上传的5个文件（focus、event、decision、idea、localisation）中的剧本设计进行修正与优化，同时根据新的剧情设计重新调整代码，然后将你修正与优化后的剧本介绍、5个文件的代码，发给我。
新的剧本设计应该突出纳塔国家内部的政治斗争、部落冲突，提高剧本的趣味性、史诗氛围、可玩性。
5个文件内的代码数量不可以改变，依旧是80个focus、80个event、30个decision、30个idea。
所有代码必须完整输出，不要简单的节选。


请你根据SAN剧情中对珊瑚宫的描述，对我上传的5个文件（focus、event、decision、idea、localisation）中的进行重写，设计一个珊瑚宫剧本，同时根据新的剧本设计重新调整代码，然后将你修正与优化后的剧本介绍、5个文件的代码，发给我。
新的剧本设计应该突出珊瑚宫国家的政治斗争、地缘冲突、与稻妻幕府的关系、与其他岛屿的关系，提高剧本的趣味性、史诗氛围、可玩性。
5个文件内的代码数量应为80个focus、80个event、30个decision、30个idea。
所有代码必须完整输出，不要简单的节选。

给下面的部分国策completion_reward中添加可能对应add_ideas = 效果，国策代码与ideas代码如下所示，如果没有对应的idea就不添加

add_ideas = 