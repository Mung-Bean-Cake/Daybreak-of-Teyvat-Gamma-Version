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