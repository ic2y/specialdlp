﻿特別聲明：

全部 Strict DLP Chinese（SDC）僅供學習交流，遵循 GUN GPL 通用公眾授權條款 (GNU General Public License) ，切勿將其用於任何非法用途！
使用前請自行估量是否有擴充安裝 Strict DLP Chinese 的需要，如果不能清楚判斷而造成之不良後果，項目組所有成員均不負任何責任！
使用SDC原始碼前務必參閱 GNU-GPL-v2.0 以及 Source-License 通用公眾授權條款之內容！


-------------------------------------------------------------------------------


Strict DLP Chinese 項目的Blog：
http://blog.sdlpc.net/

Strict DLP Chinese 項目的SourceForge頁面：
http://sourceforge.net/projects/specialdlp/

Strict DLP Chinese 項目的GitHub頁面：
https://github.com/chengr28/specialdlp/


-------------------------------------------------------------------------------


SDC與官方DLP之間的主要差別：
所有SDC均是基於Xtreme官方DLP的嚴格版本。
在Xtreme官方DLP的基礎上，SDC將VeryCD-Mod和VeryCD-EasyMule-Mod（第1版）中的部分或全部加入了SoftBan列表，原因是GPL-Breaker、私有網路和社區客戶端等不良行為。


擴充安裝方法：
1.將eMule關閉，把解壓出來的antiLeech.dll.new文件放到原來antiLeech.dll所在的目錄，並重新啟動eMule（強烈建議使用這種擴充安裝方法，因為這種方法可以把全部新版的檢測載入到eMule中，第2種方法重新載入後已經連接成功的用戶端不會被重新檢測，且新版本的所有檢測不一定都能使用。）
2.或者直接把解壓出來的antiLeech.dll.new文件放到原來antiLeech.dll所在的目錄，然後在反吸血選項（Xtreme II）中滑鼠左鍵點選「Reload」一次


關於設定文件讀取真實目錄問題：
此設定可以在安裝eMule的過程中進行選擇，不過也可以在以後任何時候在「選項->擴充設定」裡進行設定。請注意這個問題，否則可能會造成SDC未被正確載入。

1.在程式目錄下保存設定和下載：程式目錄下的Config文件夾內
2.每個使用者的設定和下載是獨立的：
 * Vista/7/8以及更新版本：%userprofile%\AppData\Local\eMule\config 亦即 System:\Users\[您的用戶名]\AppData\Local\eMule\config
 * XP/2000等舊版本：%userprofile%\Application Data\eMule\config 亦即 System:\Documents and Settings\[您的用戶名]\Application Data\eMule\config
3.所有的使用者共用相同的設定和下載（僅限Vista/7/8以及更新版本）：%AllUsersProfile%\eMule\Config 亦即 System:\ProgramData\eMule\Config


-------------------------------------------------------------------------------

SDC版本介紹：

* bin：已經編輯好的二進製程式，可以直接在電腦上使用
* src：SDC的C++啟動原始碼
提醒1：SDC基於Microsoft Visual C++ 2012 製作
提醒2：使用SDC的啟動原始碼前請認真閱讀以下使用許可協議：
       * Source-License：eMule以及Xtreme DLP的使用許可
       * GNU-GPL-v2.0：GNU通用公共許可證v2的部分副本

* x86：用於32位（x86）電腦系統的SDC版本
提醒：大多數家用電腦均為32位元，因此您應該一般使用x86版本而不是x64版本
* x64：用於64位（x64）電腦系統的SDC版本
提醒：x64的SDC版本只能用於64位元電腦系統上
注意：SDC的x64版本是專門為原生x64的eMule程式編寫，因為現階段絕大多數eMule程序的編譯目標平台為x86，所以您應該使用x86版本的SDC而非x64版本的SDC！


* Lite：Xtreme官方DLP修補漏檢版本。
* All-VeryCD-Mod：對所有VeryCD系列用戶端進行檢測的版本，其中所有 VeryCD Mod 和EasyMule被加入了軟性吸血列表。
* VeryCD-EasyMule-Mod：EasyMule被加入了軟性吸血列表。
* VeryCD-Default-NickNames：所有暱稱中含有VeryCD用戶端默認暱稱的 VeryCD Mod 和EasyMule加入到軟性吸血列表。


-------------------------------------------------------------------------------


常見問題FAQ

Q：如何查看SDC已經成功被eMule載入？
A：有2個查看方法：
* 查看反吸血選項中顯示的DLP版本號是否為SDC的最新版本號，如果不是則說明載入失敗；
* 如果不能起到SDC對應版本預期的效果，請瀏覽下面FAQ所列舉的各種情況予以參考。

Q：為何SDC的對應版本無法實現其對應的功能？
A：有2種解決方案：
* 請檢查自己選擇的版本和自己的設想是否相符；
* 請檢查是否開啟“防封禁”功能，已經開啟的請關閉“防封禁限制”功能。

Q：載入失敗如何解決？
A：有3種解決方案：
* 請檢查文件名（antiLeech.dll.new）是否完全正確；
* 請檢查antiLeech.dll.new所放置的位置是否正確，一般放置在原antiLeech.dll的目錄內；
* 請檢查對應的版本是否正確，x86/x64版本的SDC只能應用在其設計的環境內，版本之間並不通用。

Q：antiLeech.dll.old是什麼文件？能否刪除？
A：antiLeech.dll.old是被替換的DLP，當eMule發現antiLeech.dll.new時會自動將antiLeech.dll改名為antiLeech.dll.old，而同時會將antiLeech.dll.new改名為antiLeech.dll應用新版本DLP
注意：如果新版本DLP能被正常載入後，antiLeech.dll.old即可被刪除。

Q：發現了某些不應出現的誤傷或漏檢怎麼辦？
A：有2種方案：
* 請首先確認是否應用“失效搭配方案黑名單”中的搭配，應用者請更換eMule用戶端或其它系列的DLP；
 * 注意：如果使用以下搭配，將使SDC無法實現其應有正常的功能或者造成漏檢，切記不要採用以下的失效搭配：
  * eMule v0.48a eXcalibur 1.85.3 加載所有版本的SDC
    * 後果：無法成功加載DLP
    * 原因：eXcalibur不支持Xtreme官方版DLP
  * eMule 0.49b CN-7 Build 191 Final 加載所有版本的SDC
    * 後果：漏檢吸血用戶端
    * 原因：CN Mod對Xtreme官方版DLP支持不佳造成漏檢
 * 請聯繫SDC開發小組尋求解決方法：
  * SDC開發小組的Blog： http://sdlpc.net/
  * SDC開發小組的開放郵箱dev[AT]sdlpc.net 或直接聯繫核心代碼開發人員chengr28[AT]gmail.com

Q：何謂“屏蔽模式”和“減分模式”？
A：“屏蔽模式”是將對象全部忽略的意思，也就是常說的徹底封殺所有吸血騾；“減分模式”是將被定義為SoftBan的對象減少其積分的意思。

Q：如何應用“屏蔽模式”和“減分模式”？
A：應用方法：
* 屏蔽模式：請把反吸血的懲罰方式選項中全部選中“ban”或者“屏蔽”；
* 減分模式：請把反吸血的懲罰方式選項中的“社區用戶端”選為“reduce score”或者“減少積分”，其它選項均為“ban”或者“屏蔽”。

Q：使用SDC會不會影響到eMule的下載？
A：使用“屏蔽模式”時可能會有一定的影響，而使用“減分模式”時則完全不會影響eMule的下載。

Q：如果使用“減分模式”是否會錯誤對某些行為惡劣的吸血用戶端進行減分？
A：不會，因為DLP中分為“HardBan”和“SoftBan”的機制。被定義為HardBan的對象，無論反吸血參數如何設置，都會被徹底屏蔽而不會被錯誤減分
注意：受限於eMule用戶端調用DLP的順序問題，某些本應該被徹底屏蔽的用戶端可能會被錯誤減少積分，這個問題暫時無法解決。

Q：為何使用SDC的“減分模式”後發現上傳隊列依然存在大量被減分的用戶端？
A：首先需要說明的是，“減分模式”並不同於“屏蔽模式”，僅僅是依照應用DLP的eMule用戶端的初始設定來對吸血騾進行減分，並不是完全封禁。

Q：SDC會修補官方DLP的漏檢嗎？
A：當然會，只要收到官方DLP漏檢的報告，SDC小組會盡快升級以修補漏檢，同時也會通知Xtreme官方DLP的維護者盡快修復。

Q：哪裡能看到SDC完整的更新日誌？
A：從43002開始SDC就不再在編譯文件(bin)裡附帶提供更新日誌(ChangeLog)，如果需要瀏覽更新日誌，可以在SDC的源代碼(src)裡查看，或者移步SDC的項目主頁或者Blog。


應用減分模式特別技巧：

* 如果eMule用戶端擁有“每個文件一個隊列（多隊列）”功能，請將其開啟；
說明：“每個文件一個隊列（多隊列）”功能會適當對一些請求稀有文件上傳的用戶端的進行加分，而因  為上傳隊列得分是按比例扣減的，所以上傳隊列得分越高扣減的幅度也越大。

* 如果eMule用戶端支持多積分系統，建議使用“Lovelace”積分系統，然後將所有懲罰吸血騾的選項打開；
說明：選擇一個合適的積分系統有利於eMule的文件交換。
注意：選擇積分系統時切勿選擇官方積分系統！
 * 原因：官方積分系統只有獎勵機製而沒有懲罰機制，故不建議使用！

* 如果eMule用戶端擁有“不上傳給吸血用戶端”(Upload BAN)功能，請將其開啟；
說明：這個功能可以阻止對被減少積分的用戶端的上傳。
注意：部分eMule用戶端的這個功能是將上傳隊列得分置零，這並不能有效阻止對其的上傳！

* 如果應用的是“減分模式”同時eMule用戶端的減少積分幅度可以調整，請將其調整至最大；
說明：最大限度的減分幅度能有效遏制一些社區加分用戶端
提醒：一般可以調整減少積分幅度的eMule用戶端中，上傳隊列得分是按比例扣減的，所以應該將減分幅度調整為×“1”時扣減幅度最大。

* 如果eMule用戶端擁有“防封禁限制”功能，切勿將其開啟；
說明：“防封禁限制”功能是對“有貢  獻”的被屏蔽用戶端解封的功能，絕不能開啟。
後果：加載SDC基本上形同虛設

* 如果eMule用戶端轉換檢測模式（屏蔽模式、減分模式）設置完成後請馬上重啟eMule；
說明：被屏蔽的用戶端有屏蔽時間限制，而從“屏蔽模式”轉到“減分模式”時，被屏蔽的用戶端不會立刻釋放；從“減分模式”轉到“屏蔽模式”時，被減分的用戶端則不會被重新檢測而造成漏檢。所以設置完成後請馬上重啟eMule。