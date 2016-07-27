# DesignPattern
--http://rockssdlog.blogspot.tw/2012/04/design-pattern.html
--http://howard-lyrics.blogspot.tw/2011/04/design-pattern-prototype.html
    Creational
    自己做(new CTest();)、對方做(Signleton)、找另一個人做(Factory)
        -Factory
            Client端透過factory來建立物件
            舉例：飲料店，顧客只需到飲料店點餐，店員會幫你去製作那杯飲料，顧客不必管它的製造過程
        -Factory Method
            將工廠的部分也抽象化。讓每個子類別都有屬於自己工廠的類別。這樣一來會產生多個對應產品的工廠，此後擴充產品時亦要擴充相對的工廠
            舉例1：飛機，「座位艙等」分為頭等艙、商務艙、經濟艙等
            舉例2：大專面試報到，依據不同的組別找尋自己辦理的櫃檯，EX.多媒體組等
        -Prototype
            透過複製(clone)一個既有物件來取得新物件。使用時機：當製造成本太高，直接複製一個會更快
            舉例：模具，只需要透過模具就可以製造出模型，不必在去慢慢雕刻模型的形體
        -Singleton
            由類別自己造物件，client要功能 server給功能,物件建立權在server端
            可以確保同一時間只有一個實例或物件進行服務
            舉例：廁所，同一個時間只有一個人能夠使用那間廁所
    Behavioral
        -command
            封裝請求，然後進行一系列的參數化或操作
            舉例：ATM，插入金融卡、選語言、動作(領錢之類的)...
        -Observer
            觀察者模式定義了物件之間的一對多關係，如此一來，當一個物件改變狀態，其他相依者都會收到通知並自動被更新
            舉例：體重，變胖，衣服就要重新買
    Structural
        -Adapter
            規格一樣、格式不同。純界接。Adapter即是轉接器，解決介面不同的問題
            舉例：電吉他的音箱耳機"轉接頭" 3.5mm轉成6.5mm
            轉接頭：http://www.pcstore.com.tw/chengpu/M01282034.htm
        -Bridge
            規格一樣、格式相同，作法不同。傳function給人家做，但需要依照格式
            舉例：出國旅遊，可以搭船、飛機、游泳
        -Decorator
            一層包裝一層 compoent2(component1(component))
            由一個基底，透過不斷的添加東西(裝飾品)上去，產生出一個新產品
            舉例：義大利麵，麵+九層塔+蛤蠣 = 蛤蠣青醬義大利麵
        -Facade
            與adapter 2者同樣是透過另一個東西去使用一個東西
            差異在於動機，為了讓client覺得好用，將眾多class重新包裝成一個更好用的class。
            舉例：自動販賣機，使用悠遊卡消費，必須先去便利商店儲值悠遊卡，但自動販賣機，可以直接使用銅板消費，不必再先去便利商店儲值
                
