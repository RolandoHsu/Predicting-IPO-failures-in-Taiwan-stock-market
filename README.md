# FightForMasterofDegree

### 簡介 ###
撰寫碩士論文時需要使用到大量的財務資料，從資料庫抓取下來後仍需要做大量的處理，甚至是以EDA來幫助我更了解資料，因此利用Ｒ來輔助我進行資料剖析並藉此完成碩論。

### 論文方向簡介 ###
新股上市上櫃稱為IPO，在過去的研究中，不論國內外，有相當多的文獻發現IPO公司會有上市初期異常正報酬，到了長期，則呈現反轉而報酬衰減的現象。然而，卻較少有文獻提及IPO公司的失敗、下市預測。一間公司的下市，對於投資人來說，肯定是最為慘烈的情況，不僅使投資金血本無歸，更可能極大程度的影響到未來的育兒、退休等重大規劃。因此，找出可能影響IPO下市的因素即成為一個相當重要的議題。

興櫃市場是公司在進行上市櫃前，需要先在其上進行交易的市場，有點像是一個新上市櫃公司的試煉場，給予投資人投資資訊，若在興櫃市場中公司並沒有較好的表現或出現壞的紀錄（例如：重大財務危機。），則容易帶給投資人不好的印象導致交易量大減、股價暴跌甚至不容易於上市櫃中生存。而台灣，身為全世界唯一一個強制要在上市櫃前先興櫃六個月的國家，相比於其他國家，有更多的公司交易、體質資料可供研究，因而成為研究IPO下市與否的重要場所。因此我選定台灣作為研究國家，探討2002~2014年間，IPO公司的下市機率與影響因素，並透過不同的Meachine Learning Model，比較不同模型所做出的預測差異。
  
### Code特色 ###
  相比於之前所做的作品，這次撰寫Code的過程中，我採取運行方式更快的data.table來進行撰寫，之前的撰寫風格皆是利用data.frame 以及dplyr的函式進行資料處理，雖然函式好用，但資料量一大或電腦硬體不好時，容易拖慢運行速度，因而使用data.table提升運算效能。
  
###流程說明###

1. FindFirmList.Rmd

	透過 FindFirmList.Rmd 尋找符合條件的公司（EX: 挑選出2002~2014年之IPO公司，並排除金融股或興櫃期間不滿半年之公司），最終確認樣本數為659家公司。
	透過圖表等方式做EDA，探討台灣IPO公司之特性，可透過FindFirmList.html觀看結果。

2. DealWithIPOVariables.Rmd

	透過 DealWithIPOVariables.Rmd 整理所有IPO相關的變數，並將結果呈現於DealWithIPOVariables.html中。

3. FSVariables.Rmd

	透過 FSVariables.Rmd 整理IPO公司興櫃期間之財報變數，並將其與相對應的市場及產業平均比值，最終將結果呈現於 FSVariables.html 中。

4. ROTCTradingVariable.Rmd

	透過 ROTCTradingVariable.Rmd 整理所有IPO公司再興櫃期間之交易變數，例如0交易量的天數等，並將結果呈現於 ROTCTradingVariable.html。

5. BuildLogisticRegressionModel_2.Rmd

	透過BuildLogisticRegressionModel_2.Rmd 將所有變數整合後丟入 Logistic Regression 中，並將結果呈現於 BuildLogisticRegressionModel_2.html 中。
