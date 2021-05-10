# 第二章：監控與診斷網路

## 目錄

- [Security+ 中定義的術語](#security+-中定義的術語)
- [業界標準框架與參考架構](#業界標準框架與參考架構)
- [基準與安全設置指引](#基準與安全設置指引)
- [安全網路架構概念](#安全網路架構概念)
- [區域](#區域)
- [放置安全裝置](#放置安全裝置)
- [軟體定義網路](#軟體定義網路)
- [入侵檢測系統與入侵預防系統](#入侵檢測系統與入侵預防系統)
- [安全系統設計](#安全系統設計)
- [硬體與韌體安全](#硬體與韌體安全)
- [作業系統](#作業系統)
- [週邊](#週邊)
- [安全階段部屬概念](#安全階段部屬概念)

## 正文

### Security+ 中定義的術語

以下的術語解釋皆出自參考書翻譯而成

> 我覺得我翻的跟機翻差不多，如果你有其他解釋，那就用你自己的會比較好理解。

| 術語                                          | 解釋                                                                                                             |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Demilitarized Zone (DMZ)                      | 非軍事區，一個夾在兩面防火牆中的網路空間，使得公開網路與私有網路都能存取，通常 Web Server 會擺在裡面以讓外界存取 |
| Honeypot                                      | 蜜罐，一個偽造的網路空間，用以誘騙攻擊者攻擊錯誤的目標，通常還會將過程記錄下來（Logging）和跟蹤（Tracking）      |
| Honeynet                                      | 和蜜罐原理相同的網路環境                                                                                         |
| Information Security Management System (ISMS) | 資訊安全管理系統                                                                                                 |
| Intrusion Detection System (IDS)              | 入侵檢測系統                                                                                                     |
| Intrusion Prevention System (IPS)             | 入侵預防系統                                                                                                     |
| Personally Identifiable Information (PII)     | 個人可識別資訊，就是能夠用來辨識個人的資訊                                                                       |
| Software-Defined Network (SDN)                | 軟體定義網路，所有網路設施與安全設施都是虛擬的網路環境                                                           |
| Stateful Packet Inspection (SPI)              | 狀態封包檢查，持續對通過防火牆的封包進行檢查，通常是狀態防火牆（Stateful Firewall）的功能之一                    |

### 業界標準框架與參考架構

在業界有一些有關網路安全的標準、框架和指導方針，下面舉幾項重要的說明：

- **ISO 標準** ：

  - **ISO/IEC 27001:2013**是國際標準化組織（ISO）制定有關資訊安全的標準，其中提到了在組織中實作、維持和持續改進資訊安全管理系統的要求，也包含了分析並解決資安風險的要求。這個標準不僅僅要求對組織內部進行檢視，任何與組織有關的合作夥伴都應該被納入檢視。這份標準只是提供一個大方向，並沒有提供 To Do List。
  - **ISO 27002**是有關資訊安全的標準，其中提供開始、實作與維護資訊安全系統的建議。從第五章開始，每一章均提供了資訊安全管理系統不同面向的的最好做法：

    CH5. Information Security Policies（資訊安全原則）  
    CH6. Organization of Information Security（資訊安全組織）  
    CH7. Human Resource Security（人力資源安全）  
    CH8. Asset Management（資產管理）  
    CH9. Access Control（存取控制）  
    CH10. Cryptography（加密學）  
    CH11. Physical and Environmental Security（實體與環境安全）  
    CH12. Operation Security: Procedures and Responsibilities（行動安全：做法與責任）  
    CH13. Communication Security（通訊安全）  
    CH14. System Acquisition, Development and Maintenance（系統取得、建構與維護）  
    CH15. Supplier Relationships（供應商關係）  
    CH16. Information Security Incident Management（資訊安全事故管理）  
    CH17. Information Security Aspects of Business Continuity Management（業務延續性管理方面的資訊安全）

  - **ISO 27017**是有關雲端安全的指引，包含了27002中的指引外還多了7個控制內容：

    CLD.6.3.1 提到有關客戶與雲端提供者之間的合約，包含共同的與個別的責任。  
    CLD.8.1.5 提到當合約終止時資產該如何返還獲從雲端中清除。  
    CLD.9.5.1 提到雲端提供者需要將每個客戶的虛擬環境與其他客戶隔離。  
    CLD.9.5.2 提到雲端提供者與客戶都需要增強虛擬機器的穩固。  
    CLD.12.1.5 定義與管理行動完全是客戶的責任。  
    CLD.12.4.5 雲端提供者必須要有能力讓其客戶能監視他們自己的雲端環境。  
    CLD.13.1.4 虛擬網路環境的安全原則需要被配置成至少與實體環境相同。  

  - **ISO 27018**跟ISO 27017高度相關，定義了在雲端環境下的隱私要求，特別著重在雲端提供者與客戶需要保護PII。

- **北美電力可靠性公司（NERC）** ：就跟它的名字有關，他的東西基本上都跟電有關，但他也有出一個 NERC Cybersecurity Standards (CSS) 來規範網路安全。

- **美國國家標準暨技術研究院（NIST）** ：可以把他當做美國的ISO，NIST SP是NIST出版的標準，

- **支付卡行業數據安全標準（PCI-DSS）** ：

- **開放式網路應用程式安全專案（OWASP）** ：就是平常在做資安檢測時會用到的工具（OWASP Zap）

### 基準與安全設置指引

### 安全網路架構概念

### 區域

### 放置安全裝置

### 軟體定義網路

### 入侵檢測系統與入侵預防系統

### 安全系統設計

### 硬體與韌體安全

### 作業系統

### 週邊

### 安全階段部屬概念
