getgenv().Config = {
	Main = {

		Weapon = "Melee",
		FastAttack = true,
		BringMonster = true,
		AutoHaki = true,
		Code = true,

		AutoFarm = true,
		AutoFarmFast = true,

		PointStats = 1,
		Select_Stats = nil, 
	},
}

W1 = false
W2 = false
W3 = false
if game.PlaceId == 2753915549 then
	W1 = true
elseif game.PlaceId == 4442272183 then
	W2 = true
elseif game.PlaceId == 7449423635 then
	W3 = true
end

function CheckQuest()
	local MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
	if game.PlaceId == 2753915549 then
		if MyLevel == 1 or MyLevel <= 9 then -- Bandit
			Mon = "Bandit [Lv. 5]"
			NameQuest = "BanditQuest1"
			LevelQuest = 1
			NameMon = "Bandit"
			CFrameQuest = CFrame.new(1061.66699, 16.5166187, 1544.52905, -0.942978859, -3.33851502e-09, 0.332852632, 7.04340497e-09, 1, 2.99841325e-08, -0.332852632, 3.06188177e-08, -0.942978859)
			CFrameMon = CFrame.new(1057.55151, 27.1278248, 1564.76013, -0.16377756, -1.13282092e-10, -0.986497283, 3.48445752e-08, 1, -5.89970339e-09, 0.986497283, -3.53403173e-08, -0.16377756)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 10 or MyLevel <= 14 then -- Bandit
			Mon = "Monkey [Lv. 14]"
			NameQuest = "JungleQuest"
			LevelQuest = 1
			NameMon = "Monkey"
			CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
			CFrameMon = CFrame.new(-1449.94617, 67.9777908, 12.3050404, -0.643440843, 2.02988506e-08, 0.765495837, 2.12389017e-09, 1, -2.4732012e-08, -0.765495837, -1.42877576e-08, -0.643440843)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 15 or MyLevel <= 29 then -- Gorilla
			Mon = "Gorilla [Lv. 20]"
			NameQuest = "JungleQuest"
			LevelQuest = 2
			NameMon = "Gorilla"
			CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
			CFrameMon = CFrame.new(-1142.0293, 40.5877495, -516.118103, 0.55559355, 7.58965513e-08, 0.831454039, 1.24594361e-08, 1, -9.96073553e-08, -0.831454039, 6.57006538e-08, 0.55559355)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 30 or MyLevel <= 39 then -- Pirat
			Mon = "Pirate [Lv. 35]"
			NameQuest = "BuggyQuest1"
			LevelQuest = 1
			NameMon = "Pirate"
			CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
			CFrameMon = CFrame.new(-1151.29663, 44.207077, 3873.34937, -0.879714787, 3.81559784e-10, 0.475501686, -2.18363772e-09, 1, -4.84233453e-09, -0.475501686, -5.29819655e-09, -0.879714787)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 40 or MyLevel <= 59 then -- Brute
			Mon = "Brute [Lv. 45]"
			NameQuest = "BuggyQuest1"
			LevelQuest = 2
			NameMon = "Brute"
			CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
			CFrameMon = CFrame.new(-1131.66699, 14.3651161, 4191.79199, -0.968309462, -1.36864942e-09, 0.24975352, -9.80991288e-09, 1, -3.25536256e-08, -0.24975352, -3.3972043e-08, -0.968309462)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 60 or MyLevel <= 74 then -- Desert Bandit
			Mon = "Desert Bandit [Lv. 60]"
			NameQuest = "DesertQuest"
			LevelQuest = 1
			NameMon = "Desert Bandit"
			CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
			CFrameMon = CFrame.new(1054.79053, 52.5889473, 4490.35693, 0.280815929, -6.18912255e-09, 0.95976162, 4.50181625e-09, 1, 5.13142062e-09, -0.95976162, 2.87968605e-09, 0.280815929)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 75 or MyLevel <= 89 then -- Desert Officre
			Mon = "Desert Officer [Lv. 70]"
			NameQuest = "DesertQuest"
			LevelQuest = 2
			NameMon = "Desert Officer"
			CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
			CFrameMon = CFrame.new(1658.0708, 10.0252256, 4452.83154, 0.826960921, -2.71145932e-08, 0.562259436, -9.74775904e-09, 1, 6.25611705e-08, -0.562259436, -5.72164147e-08, 0.826960921)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 90 or MyLevel <= 99 then -- Snow Bandits
			Mon = "Snow Bandit [Lv. 90]"
			NameQuest = "SnowQuest"
			LevelQuest = 1
			NameMon = "Snow Bandits"
			CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
			CFrameMon = CFrame.new(1381.81982, 88.3774796, -1395.56738, -0.0662302524, 5.15531262e-08, 0.997804344, 3.78975749e-08, 1, -4.91510797e-08, -0.997804344, 3.45590756e-08, -0.0662302524)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 100 or MyLevel <= 119 then -- Snowman
			Mon = "Snowman [Lv. 100]"
			NameQuest = "SnowQuest"
			LevelQuest = 2
			NameMon = "Snowman"
			CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
			CFrameMon = CFrame.new(1171.65784, 106.437271, -1514.53918, -0.726554573, 7.11920691e-08, -0.687108815, 6.82555807e-08, 1, 3.14370361e-08, 0.687108815, -2.40582896e-08, -0.726554573)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 120 or MyLevel <= 149 then -- Chief Petty Officer
			Mon = "Chief Petty Officer [Lv. 120]"
			NameQuest = "MarineQuest2"
			LevelQuest = 1
			NameMon = "Chief Petty Officer"
			CFrameQuest = CFrame.new(-5035.0835, 28.6520386, 4325.29443, 0.0243340395, -7.08064647e-08, 0.999703884, -6.36926814e-08, 1, 7.23777944e-08, -0.999703884, -6.54350671e-08, 0.0243340395)
			CFrameMon = CFrame.new(-4908.62207, 51.0889473, 4296.17578, 0.851993144, 6.76871537e-08, -0.523552954, -6.00756422e-08, 1, 3.15213882e-08, 0.523552954, 4.59677496e-09, 0.851993144)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 150 or MyLevel <= 174 then -- Sky Bandit
			Mon = "Sky Bandit [Lv. 150]"
			NameQuest = "SkyQuest"
			LevelQuest = 1
			NameMon = "Sky Bandit"
			CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
			CFrameMon = CFrame.new(-4971.60254, 364.723907, -2860.88965, -0.967084885, 8.0616207e-09, 0.254453957, 1.28277495e-08, 1, 1.7071466e-08, -0.254453957, 1.97736281e-08, -0.967084885)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 175 or MyLevel <= 189 then -- Dark Master
			Mon = "Dark Master [Lv. 175]"
			NameQuest = "SkyQuest"
			LevelQuest = 2
			NameMon = "Dark Master"
			CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
			CFrameMon = CFrame.new(-5234.49463, 472.219452, -2260.2998, 0.0978341922, 4.7624173e-08, -0.99520272, 1.3983859e-07, 1, 6.16006801e-08, 0.99520272, -1.45194406e-07, 0.0978341922)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 190 or MyLevel <= 209 then
			Mon = "Prisoner [Lv. 190]"
			NameQuest = "PrisonerQuest"
			LevelQuest = 1
			NameMon = "Prisoner"
			CFrameQuest = CFrame.new(5308.5595703125, 1.655185341835022, 475.2810363769531 )
			CFrameMon = CFrame.new(5282.37548828125, 15.651934623718262, 356.1692810058594)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 210 or MyLevel <= 249 then
			Mon = "Dangerous Prisoner [Lv. 210]"
			NameQuest = "PrisonerQuest"
			LevelQuest = 2
			NameMon = "Dangerous Prisoner"
			CFrameQuest = CFrame.new(5308.5595703125, 1.655185341835022, 475.2810363769531 )
			CFrameMon = CFrame.new(5549.43359375, 15.635162353515625, 868.7542724609375)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 250 or MyLevel <= 274 then -- Toga Warrior
			Mon = "Toga Warrior [Lv. 250]"
			NameQuest = "ColosseumQuest"
			LevelQuest = 1
			NameMon = "Toga Warrior"
			CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
			CFrameMon = CFrame.new(-1716.77588, 105.825844, -2809.25977, -0.188207448, 2.83339467e-08, 0.982129276, 1.10813891e-08, 1, -2.67259583e-08, -0.982129276, 5.85333249e-09, -0.188207448)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 275 or MyLevel <= 299 then -- Gladiato
			Mon = "Gladiator [Lv. 275]"
			NameQuest = "ColosseumQuest"
			LevelQuest = 2
			NameMon = "Gladiato"
			CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
			CFrameMon = CFrame.new(-1440.1282958984375, 7.567874431610107, -3171.48388671875)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 300 or MyLevel <= 324 then -- Military Soldier
			Mon = "Military Soldier [Lv. 300]"
			NameQuest = "MagmaQuest"
			LevelQuest = 1
			NameMon = "Military Soldier"
			CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
			CFrameMon = CFrame.new(-5334.42627, 50.9436913, 8647.35156, -0.54487282, 0, 0.838518679, 0, 1, 0, -0.838518679, 0, -0.54487282)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 325 or MyLevel <= 374 then -- Military Spy
			Mon = "Military Spy [Lv. 325]"
			NameQuest = "MagmaQuest"
			LevelQuest = 2
			NameMon = "Military Spy"
			CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
			CFrameMon = CFrame.new(-5772.66113, 81.4496155, 8722.71973, 0.0485868454, 5.5336308e-08, 0.998818934, 6.85331543e-08, 1, -5.8735484e-08, -0.998818934, 7.13059833e-08, 0.0485868454)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 375 or MyLevel <= 399 then -- Fishman Warrior
			FM = true
			Mon = "Fishman Warrior [Lv. 375]"
			NameQuest = "FishmanQuest"
			LevelQuest = 1
			NameMon = "Fishman Warrior"
			CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
			CFrameMon = CFrame.new(60955.0625, 48.7988472, 1543.7168, -0.831178129, 6.20639318e-09, -0.556006253, 7.20035302e-08, 1, -9.64761853e-08, 0.556006253, -1.20223305e-07, -0.831178129)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
			end
		elseif MyLevel == 400 or MyLevel <= 449 then -- Fishman Commando
			FM = true
			Mon = "Fishman Commando [Lv. 400]"
			NameQuest = "FishmanQuest"
			LevelQuest = 2
			NameMon = "Fishman Commando"
			CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
			CFrameMon = CFrame.new(61872.3008, 75.5976562, 1394.83484, -0.922134459, 4.36911973e-09, -0.38686946, -2.54707899e-08, 1, 7.20052e-08, 0.38686946, 7.62523484e-08, -0.922134459)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
			end
		elseif MyLevel == 450 or MyLevel <= 474 then -- God's Guards
			FM = false
			Mon = "God's Guard [Lv. 450]"
			NameQuest = "SkyExp1Quest"
			LevelQuest = 1
			NameMon = "God's Guards"
			CFrameQuest = CFrame.new(-4721.71436, 845.277161, -1954.20105, -0.999277651, -5.56969759e-09, 0.0380011722, -4.14751478e-09, 1, 3.75035256e-08, -0.0380011722, 3.73188307e-08, -0.999277651)
			CFrameMon = CFrame.new(-4719.61719, 853.174927, -1935.9231, 0.871468067, -2.79222032e-08, 0.49045223, 3.73774967e-08, 1, -9.48327372e-09, -0.49045223, 2.6596247e-08, 0.871468067)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
			end
		elseif MyLevel == 475 or MyLevel <= 524 then -- Shandas
			sky = false
			Mon = "Shanda [Lv. 475]"
			NameQuest = "SkyExp1Quest"
			LevelQuest = 2
			NameMon = "Shandas"
			CFrameQuest = CFrame.new(-7863.63672, 5545.49316, -379.826324, 0.362120807, -1.98046344e-08, -0.93213129, 4.05822291e-08, 1, -5.48095125e-09, 0.93213129, -3.58431969e-08, 0.362120807)
			CFrameMon = CFrame.new(-7661.34229, 5548.00732, -506.59787, 0.0389961377, 4.86564531e-08, 0.999239385, -1.10884022e-08, 1, -4.82607554e-08, -0.999239385, -9.1979846e-09, 0.0389961377)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
			end
		elseif MyLevel == 525 or MyLevel <= 549 then -- Royal Squad
			sky = true
			Mon = "Royal Squad [Lv. 525]"
			NameQuest = "SkyExp2Quest"
			LevelQuest = 1
			NameMon = "Royal Squad"
			CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
			CFrameMon = CFrame.new(-7646.49707, 5608.40625, -1422.51074, 0.901955545, 9.02816666e-08, 0.431828916, -7.36900176e-08, 1, -5.51527428e-08, -0.431828916, 1.7923842e-08, 0.901955545)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 550 or MyLevel <= 624 then -- Royal Soldier
			Dis = 240
			sky = true
			Mon = "Royal Soldier [Lv. 550]"
			NameQuest = "SkyExp2Quest"
			LevelQuest = 2
			NameMon = "Royal Soldier"
			CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
			CFrameMon = CFrame.new(-8004.89062, 5645.15723, -1960.63599, 0.805200279, 3.47631635e-09, 0.593002975, -2.96576697e-09, 1, -1.83520144e-09, -0.593002975, -2.8100397e-10, 0.805200279)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 625 or MyLevel <= 649 then -- Galley Pirate
			Dis = 240
			sky = false
			Mon = "Galley Pirate [Lv. 625]"
			NameQuest = "FountainQuest"
			LevelQuest = 1
			NameMon = "Galley Pirate"
			CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
			CFrameMon = CFrame.new(5618.82129, 152.426666, 3994.08472, 0.926358402, 2.57817536e-08, 0.3766433, 1.30540767e-09, 1, -7.16620505e-08, -0.3766433, 6.68764102e-08, 0.926358402)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel >= 650 then -- Galley Captain
			Dis = 240
			Mon = "Galley Captain [Lv. 650]"
			NameQuest = "FountainQuest"
			LevelQuest = 2
			NameMon = "Galley Captain"
			CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
			CFrameMon = CFrame.new(5804.62451, 54.212822, 4895.91602, -0.889353693, -2.71176837e-09, -0.457219929, 2.99581409e-08, 1, -6.42035687e-08, 0.457219929, -7.07971424e-08, -0.889353693)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		end
	elseif game.PlaceId == 4442272183 then
		if MyLevel == 700 or MyLevel <= 724 then
			Mon = "Raider [Lv. 700]"
			LevelQuest = 1
			NameQuest = "Area1Quest"
			NameMon = "Raider"
			CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
			CFrameMon = CFrame.new(-737.026123, 39.1748352, 2392.57959)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 725 or MyLevel <= 774 then
			Mon = "Mercenary [Lv. 725]"
			LevelQuest = 2
			NameQuest = "Area1Quest"
			NameMon = "Mercenary"
			CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
			CFrameMon = CFrame.new(-960.12384, 80.2886276, 1691.82996, 0.920708776, 8.58963034e-09, -0.390250295, -3.26311032e-08, 1, -5.49752599e-08, 0.390250295, 6.33505053e-08, 0.920708776)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 775 or MyLevel <= 799 then
			Mon = "Swan Pirate [Lv. 775]"
			LevelQuest = 1
			NameQuest = "Area2Quest"
			NameMon = "Swan Pirate"
			CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898, 0.139203906, 0, 0.99026376, 0, 1, 0, -0.99026376, 0, 0.139203906)
			CFrameMon = CFrame.new(970.369446, 142.653198, 1217.3667)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 800 or MyLevel <= 874 then
			Mon = "Factory Staff [Lv. 800]"
			NameQuest = "Area2Quest"
			LevelQuest = 2
			NameMon = "Factory Staff"
			CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
			CFrameMon = CFrame.new(506.323364, 72.9597626, 9.77466297, -0.339674324, -7.69937536e-09, -0.940543115, -3.40559581e-08, 1, 4.11311296e-09, 0.940543115, 3.34282184e-08, -0.339674324)
		elseif MyLevel == 875 or MyLevel <= 899 then
			Mon = "Marine Lieutenant [Lv. 875]"
			LevelQuest = 1
			NameQuest = "MarineQuest3"
			NameMon = "Marine Lieutenant"
			CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
			CFrameMon = CFrame.new(-2682.18726, 198.169113, -2991.05737, 0.600202382, 6.21085405e-09, 0.799848199, -5.2549618e-09, 1, -3.82174248e-09, -0.799848199, -1.9093529e-09, 0.600202382)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 900 or MyLevel <= 949 then
			Mon = "Marine Captain [Lv. 900]"
			LevelQuest = 2
			NameQuest = "MarineQuest3"
			NameMon = "Marine Captain"
			CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
			CFrameMon = CFrame.new(-1860.27209, 197.220596, -3219.6062, 0.816204965, 2.98379241e-08, -0.577762485, -9.47813916e-08, 1, -8.22537274e-08, 0.577762485, 1.21897031e-07, 0.816204965)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 950 or MyLevel <= 974 then
			Mon = "Zombie [Lv. 950]"
			LevelQuest = 1
			NameQuest = "ZombieQuest"
			NameMon = "Zombie"
			CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
			CFrameMon = CFrame.new(-5634.83838, 126.067039, -697.665039)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 975 or MyLevel <= 999 then
			Mon = "Vampire [Lv. 975]"
			LevelQuest = 2
			NameQuest = "ZombieQuest"
			NameMon = "Vampire"
			CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
			CFrameMon = CFrame.new(-6030.32031, 6.4377408, -1313.5564)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1000 or MyLevel <= 1049 then
			Mon = "Snow Trooper [Lv. 1000]"
			LevelQuest = 1
			NameQuest = "SnowMountainQuest"
			NameMon = "Snow Trooper"
			CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
			CFrameMon = CFrame.new(535.893433, 401.457062, -5329.6958)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1050 or MyLevel <= 1099 then
			Mon = "Winter Warrior [Lv. 1050]"
			LevelQuest = 2
			NameQuest = "SnowMountainQuest"
			NameMon = "Winter Warrior"
			CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
			CFrameMon = CFrame.new(1223.7417, 454.575226, -5170.02148)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1100 or MyLevel <= 1124 then
			Mon = "Lab Subordinate [Lv. 1100]"
			LevelQuest = 1
			NameQuest = "IceSideQuest"
			NameMon = "Lab Subordinate"
			CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
			CFrameMon = CFrame.new(-5769.2041, 37.9288292, -4468.38721)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1125 or MyLevel <= 1174 then
			Mon = "Horned Warrior [Lv. 1125]"
			LevelQuest = 2
			NameQuest = "IceSideQuest"
			NameMon = "Horned Warrior"
			CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
			CFrameMon = CFrame.new(-6400.85889, 24.7645149, -5818.63574)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1175 or MyLevel <= 1199 then
			Mon = "Magma Ninja [Lv. 1175]"
			LevelQuest = 1
			NameQuest = "FireSideQuest"
			NameMon = "Magma Ninja"
			CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
			CFrameMon = CFrame.new(-5496.65576, 58.6890411, -5929.76855)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1200 or MyLevel <= 1249 then
			Mon = "Lava Pirate [Lv. 1200]"
			LevelQuest = 2
			NameQuest = "FireSideQuest"
			NameMon = "Lava Pirate"
			CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
			CFrameMon = CFrame.new(-5169.71729, 34.1234779, -4669.73633)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1250 or MyLevel <= 1274 then
			Mon = "Ship Deckhand [Lv. 1250]"
			LevelQuest = 1
			NameQuest = "ShipQuest1"
			NameMon = "Ship Deckhand"
			CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)         
			CFrameMon = CFrame.new(1181.84875, 130.485107, 33005.4961, -0.946877539, -7.47373434e-08, -0.321594298, -7.391602e-08, 1, -1.47637005e-08, 0.321594298, 9.79155601e-09, -0.946877539)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1275 or MyLevel <= 1299 then
			Mon = "Ship Engineer [Lv. 1275]"
			LevelQuest = 2
			NameQuest = "ShipQuest1"
			NameMon = "Ship Engineer"
			CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)        
			CFrameMon = CFrame.new(919.250427, 43.544014, 32781.9922, 0.999619186, 4.03968698e-08, -0.0275939237, -3.75240887e-08, 1, 1.04626984e-07, 0.0275939237, -1.03551706e-07, 0.999619186)       
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1300 or MyLevel <= 1324 then
			Mon = "Ship Steward [Lv. 1300]"
			LevelQuest = 1
			NameQuest = "ShipQuest2"
			NameMon = "Ship Steward"
			CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)         
			CFrameMon = CFrame.new(917.478882, 129.556, 33441.2227, -0.999965012, -1.84493896e-08, -0.00836863648, -1.84426696e-08, 1, -8.80260864e-10, 0.00836863648, -7.2589007e-10, -0.999965012)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1325 or MyLevel <= 1349 then
			Mon = "Ship Officer [Lv. 1325]"
			LevelQuest = 2
			NameQuest = "ShipQuest2"
			NameMon = "Ship Officer"
			CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)
			FrameMon = CFrame.new(1201.18286, 181.149124, 33308.0508, 0.0748318806, -7.14178512e-08, -0.997196138, 2.97970733e-08, 1, -6.93826223e-08, 0.997196138, -2.45214959e-08, 0.0748318806)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1350 or MyLevel <= 1374 then
			Mon = "Arctic Warrior [Lv. 1350]"
			LevelQuest = 1
			NameQuest = "FrostQuest"
			NameMon = "Arctic Warrior"
			CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
			CFrameMon = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1375 or MyLevel <= 1424 then
			Mon = "Snow Lurker [Lv. 1375]"
			LevelQuest = 2
			NameQuest = "FrostQuest"
			NameMon = "Snow Lurker"
			CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
			CFrameMon = CFrame.new(5518.00684, 60.5559731, -6828.80518)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1425 or MyLevel <= 1449 then
			Mon = "Sea Soldier [Lv. 1425]"
			LevelQuest = 1
			NameQuest = "ForgottenQuest"
			NameMon = "Sea Soldier"
			CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
			CFrameMon = CFrame.new(-3366.32958984375, 47.21970748901367, -9704.3505859375)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel >= 1450 then
			Mon = "Water Fighter [Lv. 1450]"
			LevelQuest = 2
			NameQuest = "ForgottenQuest"
			NameMon = "Water Fighter"
			CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
			CFrameMon = CFrame.new(-3436.7727050781, 290.52191162109, -10503.438476563)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		end
	elseif game.PlaceId == 7449423635 then
		if MyLevel == 1500 or MyLevel <= 1524 then
			Mon = "Pirate Millionaire [Lv. 1500]"
			LevelQuest = 1
			NameQuest = "PiratePortQuest"
			NameMon = "Pirate Millionaire"
			CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
			CFrameMon = CFrame.new(-290.674988, 34.7821121, 5417.57666, -0.959131062, 7.87279077e-08, 0.282962203, 6.99472977e-08, 1, -4.11336849e-08, -0.282962203, -1.96601544e-08, -0.959131062)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1525 or MyLevel <= 1574 then
			Mon = "Pistol Billionaire [Lv. 1525]"
			LevelQuest = 2
			NameQuest = "PiratePortQuest"
			NameMon = "Pistol Billionaire"
			CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
			CFrameMon = CFrame.new(-387.624237, 74.2720413, 5851.84473, -0.990750372, -6.79122536e-08, 0.135697171, -7.2516066e-08, 1, -2.89841076e-08, -0.135697171, -3.85562409e-08, -0.990750372)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1575 or MyLevel <= 1599 then
			Mon = "Dragon Crew Warrior [Lv. 1575]"
			LevelQuest = 1
			NameQuest = "AmazonQuest"
			NameMon = "Dragon Crew Warrior"
			CFrameQuest = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
			CFrameMon = CFrame.new(6241.9951171875, 51.522083282471, -1243.9771728516)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1600 or MyLevel <= 1624 then 
			Mon = "Dragon Crew Archer [Lv. 1600]"
			NameQuest = "AmazonQuest"
			LevelQuest = 2
			NameMon = "Dragon Crew Archer"
			CFrameQuest = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
			CFrameMon = CFrame.new(6788.97461, 462.341248, 164.233673, -0.711975694, 1.98202414e-08, 0.702204108, -1.45830699e-08, 1, -4.30117559e-08, -0.702204108, -4.08636183e-08, -0.711975694)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1625 or MyLevel <= 1649 then
			Mon = "Female Islander [Lv. 1625]"
			NameQuest = "AmazonQuest2"
			LevelQuest = 1
			NameMon = "Female Islander"
			CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
			CFrameMon = CFrame.new(5763.98682, 848.118103, 1082.43127, 0.986172736, 2.65753979e-08, 0.165720671, -2.36233451e-08, 1, -1.97844852e-08, -0.165720671, 1.55960436e-08, 0.986172736)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1650 or MyLevel <= 1699 then 
			Mon = "Giant Islander [Lv. 1650]"
			NameQuest = "AmazonQuest2"
			LevelQuest = 2
			NameMon = "Giant Islander"
			CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
			CFrameMon = CFrame.new(4784.24561, 708.376465, 466.297485, 0.99801594, 3.11927195e-09, 0.0629619658, -5.34848299e-09, 1, 3.52371394e-08, -0.0629619658, -3.55039766e-08, 0.99801594)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1700 or MyLevel <= 1724 then
			Mon = "Marine Commodore [Lv. 1700]"
			LevelQuest = 1
			NameQuest = "MarineTreeIsland"
			NameMon = "Marine Commodore"
			CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
			PosMon = Vector3.new(2490.0844726563, 190.4232635498, -7160.0502929688)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1725 or MyLevel <= 1774 then
			Mon = "Marine Rear Admiral [Lv. 1725]"
			NameMon = "Marine Rear Admiral"
			NameQuest = "MarineTreeIsland"
			LevelQuest = 2
			CFrameQuest = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
			CFrameMon = CFrame.new(3951.3903808594, 229.11549377441, -6912.81640625)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1775 or MyLevel <= 1799 then
			Mon = "Fishman Raider [Lv. 1775]"
			LevelQuest = 1
			NameQuest = "DeepForestIsland3"
			NameMon = "Fishman Raider"
			CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)   
			CFrameMon = CFrame.new(-10322.400390625, 390.94473266602, -8580.0908203125)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1800 or MyLevel <= 1824 then
			Mon = "Fishman Captain [Lv. 1800]"
			LevelQuest = 2
			NameQuest = "DeepForestIsland3"
			NameMon = "Fishman Captain"
			CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)   
			CFrameMon = CFrame.new(-11194.541992188, 442.02795410156, -8608.806640625)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1825 or MyLevel <= 1849 then
			Mon = "Forest Pirate [Lv. 1825]"
			LevelQuest = 1
			NameQuest = "DeepForestIsland"
			NameMon = "Forest Pirate"
			CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
			CFrameMon = CFrame.new(-13225.809570313, 428.19387817383, -7753.1245117188)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1850 or MyLevel <= 1899 then
			Mon = "Mythological Pirate [Lv. 1850]"
			LevelQuest = 2
			NameQuest = "DeepForestIsland"
			NameMon = "Mythological Pirate"
			CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)   
			CFrameMon = CFrame.new(-13869.172851563, 564.95251464844, -7084.4135742188)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1900 or MyLevel <= 1924 then
			Mon = "Jungle Pirate [Lv. 1900]"
			LevelQuest = 1
			NameQuest = "DeepForestIsland2"
			NameMon = "Jungle Pirate"
			CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
			FrameMon = CFrame.new(-11982.221679688, 376.32522583008, -10451.415039063)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1925 or MyLevel <= 1974 then
			Mon = "Musketeer Pirate [Lv. 1925]"
			LevelQuest = 2
			NameQuest = "DeepForestIsland2"
			NameMon = "Musketeer Pirate"
			CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
			CFrameMon = CFrame.new(-13282.3046875, 496.23684692383, -9565.150390625)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 1975 or MyLevel <= 1999 then
			Mon = "Reborn Skeleton [Lv. 1975]"
			LevelQuest = 1
			NameQuest = "HauntedQuest1"
			NameMon = "Reborn Skeleton"
			CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
			CFrameMon = CFrame.new(-8817.880859375, 191.16761779785, 6298.6557617188)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2000 or MyLevel <= 2024 then
			Mon = "Living Zombie [Lv. 2000]"
			LevelQuest = 2
			NameQuest = "HauntedQuest1"
			NameMon = "Living Zombie"
			CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
			CFrameMon = CFrame.new(-10125.234375, 183.94705200195, 6242.013671875)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2025 or MyLevel <= 2049 then
			Mon = "Demonic Soul [Lv. 2025]"
			LevelQuest = 1
			NameQuest = "HauntedQuest2"
			NameMon = "Demonic Soul"
			CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0) 
			CFrameMon = CFrame.new(-9712.03125, 204.69589233398, 6193.322265625)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2050 or MyLevel <= 2074 then
			Mon = "Posessed Mummy [Lv. 2050]"
			LevelQuest = 2
			NameQuest = "HauntedQuest2"
			NameMon = "Posessed Mummy"
			CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0)
			CFrameMon = CFrame.new(-9545.7763671875, 69.619895935059, 6339.5615234375)    
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2075 or MyLevel <= 2099 then
			Mon = "Peanut Scout [Lv. 2075]"
			LevelQuest = 1
			NameQuest = "NutsIslandQuest"
			NameMon = "Peanut Scout"
			CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
			CFrameMon = CFrame.new(-2265.89014, 89.7506104, -10261.2197, -0.809553444, -9.26727282e-08, 0.587046146, -5.44419549e-08, 1, 8.27857534e-08, -0.587046146, 3.50595535e-08, -0.809553444)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2100 or MyLevel <= 2124 then
			Mon = "Peanut President [Lv. 2100]"
			LevelQuest = 2
			NameQuest = "NutsIslandQuest"
			NameMon = "Peanut President"
			CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
			CFrameMon = CFrame.new(-2062.11792, 86.0444489, -10481.1445, 0.834163189, -9.79785408e-09, -0.551517665, -2.60617616e-09, 1, -2.17070646e-08, 0.551517665, 1.95445864e-08, 0.834163189)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2125 or MyLevel <= 2149 then
			Mon = "Ice Cream Chef [Lv. 2125]"
			LevelQuest = 1
			NameQuest = "IceCreamIslandQuest"
			NameMon = "Ice Cream Chef"
			CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
			CFrameMon = CFrame.new(-875.441345, 107.871437, -11253.3691, 0.630182087, 5.98710486e-08, 0.776447415, -6.03229751e-08, 1, -2.81494827e-08, -0.776447415, -2.90983202e-08, 0.63018208)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2150 or MyLevel <= 2199 then
			Mon = "Ice Cream Commander [Lv. 2150]"
			LevelQuest = 2
			NameQuest = "IceCreamIslandQuest"
			NameMon = "Ice Cream Commander"
			CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
			CFrameMon = CFrame.new(-643.3078, 140.913528, -11334.7109, -0.996822715, -9.07818087e-09, 0.0796525627, -1.43212509e-08, 1, -6.52529906e-08, -0.0796525627, -6.61863808e-08, -0.996822715)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2200 or MyLevel <= 2224 then
			Mon = "Cookie Crafter [Lv. 2200]"
			LevelQuest = 1
			NameQuest = "CakeQuest1"
			NameMon = "Cookie Crafter"
			CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295, 0.957576931, -8.80302053e-08, 0.288177818, 6.9301187e-08, 1, 7.51931211e-08, -0.288177818, -5.2032135e-08, 0.957576931)
			CFrameMon = CFrame.new(-2437.66064, 133.07428, -12122.8721, 0.215197399, 2.05706883e-08, -0.976570547, -6.6551344e-08, 1, 6.39893472e-09, 0.976570547, 6.36150475e-08, 0.215197399)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2225 or MyLevel <= 2249 then
			Mon = "Cake Guard [Lv. 2225]"
			LevelQuest = 2
			NameQuest = "CakeQuest1"
			NameMon = "Cake Guard"
			CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295, 0.957576931, -8.80302053e-08, 0.288177818, 6.9301187e-08, 1, 7.51931211e-08, -0.288177818, -5.2032135e-08, 0.957576931)
			CFrameMon = CFrame.new(-1595.00916, 44.7149811, -12252.0547, -0.998557925, -6.0718726e-08, -0.0536852553, -5.64001539e-08, 1, -8.19574169e-08, 0.0536852553, -7.88113681e-08, -0.998557925)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2250 or MyLevel <= 2274 then
			Mon = "Baking Staff [Lv. 2250]"
			LevelQuest = 1
			NameQuest = "CakeQuest2"
			NameMon = "Baking Staff"
			CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391, -0.96804446, 4.22142143e-08, 0.250778586, 4.74911062e-08, 1, 1.49904711e-08, -0.250778586, 2.64211941e-08, -0.96804446)
			CFrameMon = CFrame.new(-1817.20581, 93.8077316, -12885.6309, -0.696141601, 7.12665269e-08, 0.717904449, 4.05417566e-08, 1, -5.99574506e-08, -0.717904449, -1.26337669e-08, -0.696141601)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2274 or MyLevel <= 2300 then
			Mon = "Head Baker [Lv. 2275]"
			LevelQuest = 2
			NameQuest = "CakeQuest2"
			NameMon = "Head Baker"
			CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391, -0.96804446, 4.22142143e-08, 0.250778586, 4.74911062e-08, 1, 1.49904711e-08, -0.250778586, 2.64211941e-08, -0.96804446)
			CFrameMon = CFrame.new(-2263.37744, 156.999985, -12776, 0.945995748, 2.16281637e-09, 0.324179053, -1.23387056e-09, 1, -3.0710805e-09, -0.324179053, 2.50523402e-09, 0.945995748)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2301 or MyLevel <= 2324 then
			Mon = "Cocoa Warrior [Lv. 2300]"
			LevelQuest = 1
			NameQuest = "ChocQuest1"
			NameMon = "Cocoa Warrior"
			CFrameQuest = CFrame.new(231.75, 23.9003029, -12200.292, -1, 0, 0, 0, 1, 0, 0, 0, -1)
			CFrameMon = CFrame.new(-103.987442, 141.551514, -12260.2188, 0.589523733, -3.54913752e-08, -0.80775106, 4.28455316e-08, 1, -1.26684059e-08, 0.80775106, -2.71401959e-08, 0.589523733)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2325 or MyLevel <= 2349 then
			Mon = "Chocolate Bar Battler [Lv. 2325]"
			LevelQuest = 2
			NameQuest = "ChocQuest1"
			NameMon = "Chocolate Bar Battler"
			CFrameQuest = CFrame.new(231.75, 23.9003029, -12200.292, -1, 0, 0, 0, 1, 0, 0, 0, -1)
			CFrameMon = CFrame.new(617.304688, 80.6076355, -12580.6494, -0.485228658, 3.42073503e-09, -0.874387324, -4.0368306e-08, 1, 2.63139608e-08, 0.874387324, 4.80658215e-08, -0.485228658)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2350 or MyLevel <= 2374 then
			Mon = "Sweet Thief [Lv. 2350]"
			LevelQuest = 1
			NameQuest = "ChocQuest2"
			NameMon = "Sweet Thief"
			CFrameQuest = CFrame.new(151.198242, 23.8907146, -12774.6172, 0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, 0.422592998)         
			CFrameMon = CFrame.new(72.062767, 77.630722, -12640.4287, -0.62450999, -9.80953416e-08, 0.781016827, 1.42118917e-09, 1, 1.26735927e-07, -0.781016827, 8.02578199e-08, -0.62450999)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2375 or MyLevel <= 2399 then
			Mon = "Candy Rebel [Lv. 2375]"
			LevelQuest = 2
			NameQuest = "ChocQuest2"
			NameMon = "Candy Rebel"
			CFrameQuest = CFrame.new(151.198242, 23.8907146, -12774.6172, 0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, 0.422592998)
			CFrameMon = CFrame.new(132.856018, 77.2476807, -12879.9326, 0.89512676, -3.53753471e-08, 0.445811719, 4.89449583e-08, 1, -1.89241209e-08, -0.445811719, 3.87597225e-08, 0.89512676)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel == 2400 or MyLevel <= 2424 then
			Mon = "Candy Pirate [Lv. 2400]"
			LevelQuest = 1
			NameQuest = "CandyQuest1"
			NameMon = "Candy Pirate"
			CFrameQuest = CFrame.new(-1147.69275, 16.1330471, -14445.4229, 0.054029543, -5.45906254e-08, 0.998539329, -7.67335493e-08, 1, 5.8822426e-08, -0.998539329, -7.97996194e-08, 0.054029543)
			CFrameMon = CFrame.new(-1463.33704, 49.2304688, -14636.1562, 0.729972064, 1.66953995e-09, -0.683476985, -9.82430359e-10, 1, 1.39345324e-09, 0.683476985, -3.45713347e-10, 0.729972064)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		elseif MyLevel >= 2425 then
			Mon = "Snow Demon [Lv. 2425]"
			LevelQuest = 2
			NameQuest = "CandyQuest1"
			NameMon = "Snow Demon"
			CFrameQuest = CFrame.new(-1147.69275, 16.1330471, -14445.4229, 0.054029543, -5.45906254e-08, 0.998539329, -7.67335493e-08, 1, 5.8822426e-08, -0.998539329, -7.97996194e-08, 0.054029543)
			CFrameMon = CFrame.new(-852.233948, 90.9719009, -14727.04, -0.480660468, -1.84332318e-08, 0.876906812, -5.88126792e-09, 1, 1.77970332e-08, -0.876906812, 3.39700601e-09, -0.480660468)
			if _G.AutoFarm and _G.AutoFarmFast == false and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1200 then
				Bypass(CFrameQuest)
			end
		end
	end
end

function UnEquipWeapon(Weapon)
	if game.Players.LocalPlayer.Character:FindFirstChild(Weapon) then
		_G.NotAutoEquip = true
		wait(.5)
		game.Players.LocalPlayer.Character:FindFirstChild(Weapon).Parent = game.Players.LocalPlayer.Backpack
		wait(.1)
		_G.NotAutoEquip = false
	end
end

function EquipWeapon(ToolSe)
	if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
		local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
		wait(.4)
		game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
	end
end



spawn(function()
	game:GetService("RunService").Heartbeat:Connect(function()
		if _G.AutoFarm then
			if not game:GetService("Workspace"):FindFirstChild("Part") then
				local Part = Instance.new("Part")
				Part.Name = "Part"
				Part.Parent = game.Workspace
				Part.Anchored = true
				Part.Transparency = 1
				Part.Size = Vector3.new(40,1.5,40)
			elseif game:GetService("Workspace"):FindFirstChild("Part") then
				game.Workspace["Part"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
			end
		else
			if game:GetService("Workspace"):FindFirstChild("Part") then
				game:GetService("Workspace"):FindFirstChild("Part"):Destroy()
			end
		end
	end)
end)
spawn(function()
	game:GetService("RunService").Stepped:Connect(function()
		if _G.AutoFarm then
			for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
				if v:IsA("BasePart") then
					v.CanCollide = false    
				end
			end
		end
	end)
end)
function changestate()
	game.Workspace["Part"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
end

spawn(function()
	while task.wait() do
		pcall(function()
			if _G.AutoFarm then
				if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
					local Noclip = Instance.new("BodyVelocity")
					Noclip.Name = "BodyClip"
					Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
					Noclip.MaxForce = Vector3.new(100000,100000,100000)
					Noclip.Velocity = Vector3.new(0,0,0)
				end
			else
				game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
			end
		end)
	end
end)

function CheckMaterial(matname)
	for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
		if type(v) == "table" then
			if v.Type == "Material" then
				if v.Name == matname then
					return v.Count
				end
			end
		end
	end
	return 0
end





function Hop()
	local PlaceID = game.PlaceId
	local AllIDs = {}
	local foundAnything = ""
	local actualHour = os.date("!*t").hour
	local Deleted = false
	function TPReturner()
		local Site;
		if foundAnything == "" then
			Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
		else
			Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
		end
		local ID = ""
		if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
			foundAnything = Site.nextPageCursor
		end
		local num = 0;
		for i,v in pairs(Site.data) do
			local Possible = true
			ID = tostring(v.id)
			if tonumber(v.maxPlayers) > tonumber(v.playing) then
				for _,Existing in pairs(AllIDs) do
					if num ~= 0 then
						if ID == tostring(Existing) then
							Possible = false
						end
					else
						if tonumber(actualHour) ~= tonumber(Existing) then
							local delFile = pcall(function()
								AllIDs = {}
								table.insert(AllIDs, actualHour)
							end)
						end
					end
					num = num + 1
				end
				if Possible == true then
					table.insert(AllIDs, ID)
					wait()
					pcall(function()
						wait()
						game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
					end)
					wait(4)
				end
			end
		end
	end
	function Teleport() 
		while wait() do
			pcall(function()
				TPReturner()
				if foundAnything ~= "" then
					TPReturner()
				end
			end)
		end
	end
	Teleport()
end

Code = {
	"EXP_5B",
	"CONTROL",
	"UPDATE11",
	"XMASEXP",
	"1BILLION",
	"ShutDownFix2",
	"UPD14",
	"STRAWHATMAINE",
	"TantaiGaming",
	"Colosseum",
	"Axiore",
	"Sub2Daigrock",
	"Sky Island 3",
	"Sub2OfficialNoobie",
	"SUB2NOOBMASTER123",
	"THEGREATACE",
	"Fountain City",
	"BIGNEWS",
	"FUDD10",
	"SUB2GAMERROBOT_EXP1",
	"UPD15",
	"2BILLION",
	"UPD16",
	"3BVISITS",
	"fudd10_v2",
	"Starcodeheo",
	"Magicbus",
	"JCWK",
	"Bluxxy",
	"Sub2Fer999",
	"Enyu_is_Pro"
}

spawn(function()
	game:GetService("RunService").RenderStepped:Connect(function()
		pcall(function()
			for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
				if _G.AutoFarm then
					if game:GetService("Workspace").Enemies[v.Name].Humanoid.Health == 0 then
						game:GetService("Workspace").Enemies[v.Name]:Destroy()
					end
					wait(.5)
					if game:GetService("Workspace").Enemies[v.Name].Humanoid.Health == 0 then
						game:GetService("Workspace").Enemies[v.Name]:Destroy()
					end
				end
			end
		end)
	end)
end)
spawn(function()
	while wait(5) do
		if _G.AutoFarm then
			MyLevel = game.Players.localPlayer.Data.Level.value
			if MyLevel >= 15 then
				for i,v in pairs(Code) do
					pcall(function()
						local args = {
							[1] = v
						}
						game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(unpack(args))
					end)
				end
				break
			end
		end
	end
end)

function InventorySword(Itme)
	for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
		if type(v) == "table" then
			if v.Type == "Sword" then
				if v.Name == Itme then
					return true
				end
			end
		end
	end
	return false
end

_G.Hom = 250.40
TweeSpeed = 300.50
getgenv().ToTarget = function(Point)
	local LocalPlayer = game.Players.LocalPlayer 
	repeat wait()
		TweenPlay = (Point.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if LocalPlayer.Character.Humanoid.Sit == true then 
			LocalPlayer.Character.Humanoid.Sit = false 
		end
		pcall(function() 
			tot = game:GetService("TweenService"):Create(LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(TweenPlay/TweeSpeed, Enum.EasingStyle.Linear),{CFrame = Point})
		end)
		tot:Play()
		if TweenPlay <= _G.Hom then
			tot:Cancel()
			LocalPlayer.Character.HumanoidRootPart.CFrame = Point
		end
		if _G.StopTween == true then
			tot:Cancel()
			_G.Clip = false
		end
		if not game:GetService("Workspace"):FindFirstChild("Part") then
			local Part = Instance.new("Part")
			Part.Name = "Part"
			Part.Parent = game.Workspace
			Part.Anchored = true
			Part.Transparency = 1
			Part.Size = Vector3.new(40, 0.5, 40)
		elseif game:GetService("Workspace"):FindFirstChild("Part") then
			game.Workspace["Part"].CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
		else
			game:GetService("Workspace"):FindFirstChild("Part"):Destroy()
		end
	until TweenPlay <= _G.Hom
end

function StopTween(target)
	if not target then
		_G.StopTween = true
		wait()
		getgenv().ToTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
		wait()
		if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
			game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
		end
		_G.StopTween = false
		_G.Clip = false
	end
end

function TPPlayer(Pos)
	repeat wait()
		Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
		pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/200, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
		tween:Play()
		if Distance <= 350 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
		end
		if Distance >= 1200 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.Head:Destroy()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			wait(1)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
		end
		if _G.StopTween == true then
			tween:Cancel()
			_G.Clip = false
		end
	until Distance <= 3000
end

function Bypass(Position)
	game.Players.LocalPlayer.Character.Head:Destroy()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	wait(1)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
end

local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
	vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
	wait(1)
	vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)

spawn(function()
	while true do wait()
		if setscriptable then
			setscriptable(game.Players.LocalPlayer, "SimulationRadius", true)
		end
		if sethiddenproperty then
			sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
		end
	end
end)

--Magnet
spawn(function()
	game:GetService("RunService").Heartbeat:Connect(function()
		pcall(function()
			local MyLevel = game.Players.LocalPlayer.Data.Level.Value
			if _G.AutoFarm then
				CheckQuest()
				for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
					if v.Name ~= "Ice Admiral [Lv. 700] [Boss]" and v.Name ~= "Don Swan [Lv. 3000] [Boss]" and v.Name ~= "Saber Expert [Lv. 200] [Boss]" and v.Name ~= "Longma [Lv. 2000] [Boss]" and(v.HumanoidRootPart.Position-PosMon.Position).magnitude <= 370 then --370
						v.HumanoidRootPart.CFrame = PosMon
						v.Humanoid.JumpPower = 0
						v.Humanoid.WalkSpeed = 0
						v.HumanoidRootPart.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
						v.Humanoid:ChangeState(14)
					end
				end
			elseif _G.AutoFarm then
				for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
					if (v.HumanoidRootPart.Position-PosMon.Position).magnitude <= 340 then
						v.HumanoidRootPart.CFrame = PosMon
						v.Humanoid.JumpPower = 0
						v.Humanoid.WalkSpeed = 0
						v.HumanoidRootPart.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
						v.Humanoid:ChangeState(14)
					end
				end
			end
		end)
	end)
end)

spawn(function()
	while wait() do
		if _G.AutoFarm then
			pcall(function()
				local QuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
				if not string.find(QuestTitle, NameMon) then
					StartMagnet = false
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
				end
				if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LevelQuest)
				elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
						for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
							if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
								if v.Name == Mon then
									if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
										repeat task.wait()
											AutoHaki()
											PosMon = v.HumanoidRootPart.CFrame
											topos(v.HumanoidRootPart.CFrame * CFrame.new(5,10,7))
											v.HumanoidRootPart.CanCollide = false
											v.Humanoid.WalkSpeed = 0
											v.Head.CanCollide = false
											v.HumanoidRootPart.Size = Vector3.new(100,100,100)
											StartMagnet = true
										until not _G.AutoFarm or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
									else
										StartMagnet = false
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
									end
								end
							end
						end
					else
						StartMagnet = false
						getgenv().Use = false
						if game:GetService("ReplicatedStorage"):FindFirstChild(Mon) then
							topos(game:GetService("ReplicatedStorage"):FindFirstChild(Mon).HumanoidRootPart.CFrame * CFrame.new(5,10,7))
						else
							if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 15 then
								if PosMon ~= nil then
									topos(PosMon * CFrame.new(5,10,7))
								else
									if OldPos ~= nil then
										topos(OldPos.Position)
									end
								end
							end
						end
					end
				end
			end)
		end
	end
end)

function InMyNetWork(object)
	if isnetworkowner then
		return isnetworkowner(object)
	else
		if (object.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 200 then 
			return true
		end
		return false
	end
end

if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Death") then
	game:GetService("ReplicatedStorage").Effect.Container.Death:Destroy()
end
if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Respawn") then
	game:GetService("ReplicatedStorage").Effect.Container.Respawn:Destroy()
end

spawn(function()
	while task.wait() do
		pcall(function()
			if _G.AutoFarm  then
				local MyLevel = game.Players.LocalPlayer.Data.Level.Value
				if _G.AutoFarmFast  and (MyLevel >= 15 and MyLevel <= 300) then
					if MyLevel >= 15 and MyLevel <= 300 then
						AutoFarmFast()
					end
				else
					local QuestC = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest
					BringMobFarm = false
					if QuestC.Visible == false then
						CheckQuest()
						repeat wait() getgenv().ToTarget(CFrameQuest) until (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 20 or not _G.AutoFarm
						if (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30 then
							wait(.2)
							BringMobFarm = false
							wait(.2)
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LevelQuest)
							wait(0.5)
							getgenv().ToTarget(CFrameMon)
						end
						repeat wait() getgenv().ToTarget(CFrameMon) until (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 20 or not _G.AutoFarm
					elseif QuestC.Visible == true then
						CheckQuest()
						if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
							for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
								if v.Name == Mon and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
									repeat wait()
										EquipWeapon(_G.Select_Weapon)
										v.HumanoidRootPart.CanCollide = false
										v.Humanoid.WalkSpeed = 0
										v.Head.CanCollide = false
										BringMobFarm = true
										PosMon = v.HumanoidRootPart.CFrame
										v.HumanoidRootPart.Transparency = 1
										getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
									until not _G.AutoFarm or not v.Parent or v.Humanoid.Health < 0
								else
									BringMobFarm = false
									if game:GetService("ReplicatedStorage"):FindFirstChild(Mon) then
										getgenv().ToTarget(game:GetService("ReplicatedStorage"):FindFirstChild(Mon).HumanoidRootPart.CFrame * CFrame.new( 0, 30, 5))
									else
										getgenv().ToTarget(CFrameMon)
									end
								end
							end
						end
						if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
						end
					end
				end
			end
		end)
	end
end)

function AutoFarmFast()
	pcall(function()
		local MyLevel = game.Players.LocalPlayer.Data.Level.Value
		local QuestC = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest
		CFrameMon = CFrame.new(-4837.64258, 850.10199, -1840.58374, -0.430530697, -4.42848638e-08, -0.90257591, -3.08042516e-08, 1, -3.43712756e-08, 0.90257591, 1.30052875e-08, -0.430530697)
		if MyLevel >= 15 and MyLevel <= 69 then
			BringMobFarm = false
			for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
				if v.Name == "God's Guard [Lv. 450]" then
					if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
						repeat task.wait()
							EquipWeapon(_G.Select_Weapon)
							v.HumanoidRootPart.CanCollide = false
							v.Humanoid.WalkSpeed = 0
							v.Head.CanCollide = false
							BringMobFarm = true
							PosMon = v.HumanoidRootPart.CFrame
							v.HumanoidRootPart.Transparency = 1
							if AttackRandomType == 1 then
								getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 5))
							elseif AttackRandomType == 2 then
								getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 60))
							elseif AttackRandomType == 3 then
								getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -60))
							elseif AttackRandomType == 4 then
								getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(60, 1, 0))
							elseif AttackRandomType == 5 then
								getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(-60, 1, 0))
							else
								getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 5))
							end
						until not v.Parent or not _G.AutoFarmFast or v.Humanoid.Health < 0
					end
				else
					BringMobFarm = false
					if _G.AutoFarm and _G.AutoFarmFast and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 500 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
					end
					getgenv().ToTarget(CFrameMon)
				end
			end
		elseif MyLevel >= 70 and MyLevel <= 310 then
			if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
			end
			if QuestC.Visible == false then
				if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				end
			elseif QuestC.Visible == true then
				local quest = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
				local Player = string.split(quest," ")[2]
				getgenv().SelectPly = string.split(quest," ")[2]
				if string.find(quest,"Defeat") then
					repeat task.wait()
						if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
						end
						if game:GetService("Players").LocalPlayer.PlayerGui.Main.PvpDisabled.Visible == true then
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EnablePvp")
						end
						EquipWeapon(_G.Select_Weapon)
						TPPlayer(game:GetService("Players")[getgenv().SelectPly].Character.HumanoidRootPart.CFrame*CFrame.new(1,0,1))
						game.Players:FindFirstChild(Player).Character.HumanoidRootPart.Size = Vector3.new(120,120,120)
						game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
						game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
					until game.Players:FindFirstChild(Player).Character.Humanoid.Health <= 0 or not game.Players:FindFirstChild(Player) or not FastFarm()
					if not game.Players:FindFirstChild(Player) then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
					end   
				else
					UnEquipWeapon(_G.Select_Weapon)
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")
				end
			end
		end
	end)
end

spawn(function()
	while wait() do
		if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
			if _G.AutoFarm then
				local args = {
					[1] = "StartQuest",
					[2] = NameQuest, 
					[3] = LevelQuest
				}
				game:GetService("ReplicatedStorage").Remotes.CommF:InvokeServer(unpack(args))

			end
		end
	end
end)

pcall(function()
	CheckQuest()
	if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
		for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
			if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
				if v.Name == Mon then
					if v.Humanoid.Health > 0 then
						repeat wait()
							EquipWeapon(_G.Select_Weapon)
							AutoHaki()
							PosMon = v.HumanoidRootPart.CFrame
							v.HumanoidRootPart.CanCollide = false
							v.Humanoid.WalkSpeed = 0
							v.Head.CanCollide = false
							v.HumanoidRootPart.Size = Vector3.new(50,50,50)
							BringMobFarm = true
							getgenv().ToTarget(v.HumanoidRootPart.CFrame * CFrame.new(0,20,0))
						until not _G.AutoFarm or v.Humanoid.Health <= 0 or not v.Parent
					end
				end
			end
		end
	else
		StartMagnet = false
		if game:GetService("ReplicatedStorage"):FindFirstChild(Ms) then
			topos(game:GetService("ReplicatedStorage"):FindFirstChild(Ms).HumanoidRootPart.CFrame * CFrame.new(0,20,0))
		else	
			topos(CFrameMon)
		end
	end
end)

spawn(function()
	while wait() do
		pcall(function()
			if getgenv().Config.Main.Weapon == "Melee" then
				for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
					if v.ToolTip == "Melee" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							_G.Select_Weapon = v.Name
						end
					end
				end
			end
		end)
	end
end)

_G.FastAttack = false

local plr = game.Players.LocalPlayer

local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))
local CbFw2 = CbFw[2]

function GetCurrentBlade() 
	local p13 = CbFw2.activeController
	local ret = p13.blades[1]
	if not ret then return end
	while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end
	return ret
end

function AttackNoCD() 
	local AC = CbFw2.activeController
	for i = 1, 1 do 
		local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits(
		plr.Character,
		{plr.Character.HumanoidRootPart},
		60
		)
		local cac = {}
		local hash = {}
		for k, v in pairs(bladehit) do
			if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then
				table.insert(cac, v.Parent.HumanoidRootPart)
				hash[v.Parent] = true
			end
		end
		bladehit = cac
		if #bladehit > 0 then
			local u8 = debug.getupvalue(AC.attack, 5)
			local u9 = debug.getupvalue(AC.attack, 6)
			local u7 = debug.getupvalue(AC.attack, 4)
			local u10 = debug.getupvalue(AC.attack, 7)
			local u12 = (u8 * 798405 + u7 * 727595) % u9
			local u13 = u7 * 798405
			(function()
				u12 = (u12 * u9 + u13) % 1099511627776
				u8 = math.floor(u12 / u9)
				u7 = u12 - u8 * u9
			end)()
			u10 = u10 + 1
			debug.setupvalue(AC.attack, 5, u8)
			debug.setupvalue(AC.attack, 6, u9)
			debug.setupvalue(AC.attack, 4, u7)
			debug.setupvalue(AC.attack, 7, u10)
			pcall(function()
				for k, v in pairs(AC.animator.anims.basic) do
					v:Play(0, 0, 0)
				end                  
			end)
			if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then 
				game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
				game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
				game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "") 
			end
		end
	end
end

_G.Fast_Delay = 0
_G.Fast_Attach_Toggle = true
_G.DElayAttack = 0
_G.Cooldown_Attach = true
_G.CFA = 45
spawn(function()
	while wait() do
		pcall(function()
			if _G.Fast_Attach_Toggle then
				repeat wait(_G.Fast_Delay)
					if _G.Cooldown_Attach  then
						if _G.DElayAttack == _G.CFA then
							wait(1.5)
							_G.DElayAttack = 0
						else
							AttackNoCD()
							_G.DElayAttack = _G.DElayAttack + 2
						end
					else
						AttackNoCD()
					end
				until not _G.Fast_Attach_Toggle
			end
		end)
	end
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.AutoFarm then
				if W1 then
					local args = {
						[1] = "AddPoint",
						[2] = "Melee",
						[3] = _G.Point
					}

					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				elseif W2 then
					local args = {
						[1] = "AddPoint",
						[2] = "Melee",
						[3] = _G.Point
					}

					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					local args = {
						[1] = "AddPoint",
						[2] = "Defense",
						[3] = _G.Point
					}

					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
			end
		end)
	end
end)

spawn(function()
	while task.wait() do
		pcall(function()
			if _G.AutoFarm and game:GetService("Players").LocalPlayer.Data.Level.Value <= 150 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Dual Katana")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Cutlass")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Refined Slingshot")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Refined Flintlock")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Dual-Headed Blade")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Iron Mace")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Black Cape")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Bisento")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Tomoe Ring")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Katana")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Triple Katana")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Pipe")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Soul Cane")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Tomoe Ring")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Black Cape")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Swordsman Hat")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Slingshot")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Musket")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Flintlock")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Refined Flintlock")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Cannon")
			end
		end)
	end
end)

spawn(function()
	while task.wait() do
		pcall(function()
			if _G.AutoFarm then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki","Geppo")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki","Buso")
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki","Soru")
			end
		end)
	end
end)

function FPSBOOT()
	pcall(function()
		game:GetService("Lighting").FantasySky:Destroy()
		local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
		local g = game
		local w = g.Workspace
		local l = g.Lighting
		local t = w.Terrain
		t.WaterWaveSize = 0
		t.WaterWaveSpeed = 0
		t.WaterReflectance = 0
		t.WaterTransparency = 0
		l.GlobalShadows = false
		l.FogEnd = 9e9
		l.Brightness = 0
		settings().Rendering.QualityLevel = "Level01"
		for i, v in pairs(g:GetDescendants()) do
			if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then 
				v.Material = "Plastic"
				v.Reflectance = 0
				--v.CanCollide = false
			elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
				v.Transparency = 1
			elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
				v.Lifetime = NumberRange.new(0)
			elseif v:IsA("Explosion") then
				v.BlastPressure = 1
				v.BlastRadius = 1
			elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
				v.Enabled = false
			elseif v:IsA("MeshPart") then
				v.Material = "Plastic"
				v.Reflectance = 0
				v.TextureID = 10385902758728957

			end
		end
		for i, e in pairs(l:GetChildren()) do
			if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
				e.Enabled = false
			end
		end
		for i, v in pairs(game:GetService("Workspace").Camera:GetDescendants()) do
			if v.Name == ("Water;") then
				v.Transparency = 1
				v.Material = "Plastic"
			end
		end
	end)
end

if _G.FPS_Boost then
	FPSBOOT()
end--warter

function AutoHaki()
	if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("HasBuso") then
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso");
	end
end
local DiscordLib = loadstring(game:HttpGet"https://raw.githubusercontent.com/kickTh/New-Ui/main/discord%20lib%20(1).txt")()

local win = DiscordLib:Window("discord Manake X Hub")

local serv = win:Server("Manake Hub", "")

local Main = serv:Channel("Manake X Hub")

Main:Toggle("Stats",true, function(bool)
	_G.AutoFarm = bool
end)

Main:Button("Code", function()
	for i,v in pairs(Code) do
		UseCode(v)
	end
end)

Main:Button("Fpsboot", function()
	FPSBOOT()
end)
