以Mobile做為例子來說明，理應作業系統、螢幕尺寸、品牌...等都是出廠(初始化)時就確定了，不能讓user隨意地修改;而其他屬性，像是顏色、SDK版本...等都是日後可以讓user自行去修改的。

builder模式就可以解決這種需求，如果某些method只能在初始化階段中使用，那就放在Builder的類別中，然後要產生該類別的變數都必須透過Builder類別中的build()。

為了強制要求只能用build()來產生類別變數，可以將該類別的建構子設成private。