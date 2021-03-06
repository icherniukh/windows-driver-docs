---
title: Native WLAN to WDI OID mapping
description: The following table contains the mappings between Native 802.11 WLAN and WDI OIDs.
ms.assetid: 98F4D26F-72FC-4945-AF53-064A0F80673F
ms.author: windowsdriverdev
ms.date: 04/20/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
ms.localizationpriority: medium
---

# Native WLAN to WDI OID mapping


The following table contains the mappings between Native 802.11 WLAN OIDs to WDI commands. This is not a static mapping and, depending on the current state, additional or fewer WDI commands may be sent down.

**Note**  
Due to long DDI names, you may need to scroll the table horizontally to see all content. There is a scrollbar at the bottom of the page.

| DDI | Query | Set/Method/Function |
| ---| --- | --- |
| *MIBS* |
| [OID\_DOT11\_BEACON\_PERIOD](https://msdn.microsoft.com/library/windows/hardware/ff569109) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_COUNTRY\_STRING](https://msdn.microsoft.com/library/windows/hardware/ff569123) | Unsupported | Not applicable |
| [OID\_DOT11\_CURRENT\_CHANNEL](https://msdn.microsoft.com/library/windows/hardware/ff569127) | Handled by Microsoft | Unsupported |
| [OID\_DOT11\_CURRENT\_FREQUENCY](https://msdn.microsoft.com/library/windows/hardware/ff569130) | Handled by Microsoft | Unsupported |
| [OID\_DOT11\_CURRENT\_REG\_DOMAIN](https://msdn.microsoft.com/library/windows/hardware/ff569136) | Unsupported | Not applicable |
| [OID\_DOT11\_DTIM\_PERIOD](https://msdn.microsoft.com/library/windows/hardware/ff569152) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_FRAGMENTATION\_THRESHOLD](https://msdn.microsoft.com/library/windows/hardware/ff569368) | Unsupported | Unsupported |
| [OID\_DOT11\_LONG\_RETRY\_LIMIT](https://msdn.microsoft.com/library/windows/hardware/ff569380) | Unsupported | Unsupported |
| [OID\_DOT11\_MULTI\_DOMAIN\_CAPABILITY\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569390) | Unsupported | Unsupported |
| [OID\_DOT11\_OPERATIONAL\_RATE\_SET](https://msdn.microsoft.com/library/windows/hardware/ff569395) | Handled by Microsoft | Unsupported |
| [OID\_DOT11\_REG\_DOMAINS\_SUPPORT\_VALUE](https://msdn.microsoft.com/library/windows/hardware/ff569408) | Unsupported | Not applicable |
| [OID\_DOT11\_RTS\_THRESHOLD](https://msdn.microsoft.com/library/windows/hardware/ff569411) | Unsupported | Not applicable |
| [OID\_DOT11\_SHORT\_RETRY\_LIMIT](https://msdn.microsoft.com/library/windows/hardware/ff569415) | Unsupported | Unsupported |
| *Operational* |
| [OID\_DOT11\_CURRENT\_OPERATION\_MODE](https://msdn.microsoft.com/library/windows/hardware/ff569132) | Handled by Microsoft | [OID\_WDI\_TASK\_CHANGE\_OPERATION\_MODE](https://msdn.microsoft.com/library/windows/hardware/dn925946) |
| [OID\_DOT11\_MULTICAST\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569388) | Handled by Microsoft | [OID\_WDI\_SET\_MULTICAST\_LIST](https://msdn.microsoft.com/library/windows/hardware/dn925932) |
| [OID\_DOT11\_NIC\_POWER\_STATE](https://msdn.microsoft.com/library/windows/hardware/ff569392) | Handled by Microsoft | [OID\_WDI\_TASK\_DOT11\_RESET](https://msdn.microsoft.com/library/windows/hardware/dn925952), [OID\_WDI\_TASK\_SET\_RADIO\_STATE](https://msdn.microsoft.com/library/windows/hardware/dn925963) |
| [OID\_DOT11\_NIC\_SPECIFIC\_EXTENSION](https://msdn.microsoft.com/library/windows/hardware/ff569393) | Not applicable | [OID\_WDI\_IHV\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/dn925851) |
| [OID\_DOT11\_RESET\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569409) | Not applicable | [OID\_WDI\_TASK\_DOT11\_RESET](https://msdn.microsoft.com/library/windows/hardware/dn925952) |
| [OID\_DOT11\_SCAN\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569413) | Not applicable | [OID\_WDI\_TASK\_SCAN](https://msdn.microsoft.com/library/windows/hardware/dn925959) |
| *Virtual Wi-Fi* |
| [OID\_DOT11\_CREATE\_MAC](https://msdn.microsoft.com/library/windows/hardware/ff569124) | Not applicable | [OID\_WDI\_TASK\_CREATE\_PORT](https://msdn.microsoft.com/library/windows/hardware/dn925949), [OID\_WDI\_TASK\_DOT11\_RESET](https://msdn.microsoft.com/library/windows/hardware/dn925952) |
| [OID\_DOT11\_DELETE\_MAC](https://msdn.microsoft.com/library/windows/hardware/ff569140) | Not applicable | [OID\_WDI\_TASK\_DOT11\_RESET](https://msdn.microsoft.com/library/windows/hardware/dn925952), [OID\_WDI\_TASK\_DELETE\_PORT](https://msdn.microsoft.com/library/windows/hardware/dn925950) |
| [OID\_DOT11\_VIRTUAL\_STATION\_CAPABILITY](https://msdn.microsoft.com/library/windows/hardware/ff569435) | **No planned support** |  |
| *ExtSTA/ExtAP* |
| [OID\_DOT11\_ACTIVE\_PHY\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569102) | Handled by Microsoft based on [**WDI\_TLV\_ASSOCIATION\_RESULT**](https://msdn.microsoft.com/library/windows/hardware/dn926140) |  |
| [OID\_DOT11\_ASSOCIATION\_PARAMS](https://msdn.microsoft.com/library/windows/hardware/ff569104) | Not applicable | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_AUTO\_CONFIG\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569106) | Handled by Microsoft | Handled by Microsoft |
| [OID\_DOT11\_CIPHER\_DEFAULT\_KEY](https://msdn.microsoft.com/library/windows/hardware/ff569119) | Not applicable | [OID\_WDI\_SET\_ADD\_CIPHER\_KEYS](https://msdn.microsoft.com/library/windows/hardware/dn925855) |
| [OID\_DOT11\_CIPHER\_DEFAULT\_KEY\_ID](https://msdn.microsoft.com/library/windows/hardware/ff569120) | Handled by Microsoft | [OID\_WDI\_SET\_DEFAULT\_KEY\_ID](https://msdn.microsoft.com/library/windows/hardware/dn925928) |
| [OID\_DOT11\_CIPHER\_KEY\_MAPPING\_KEY](https://msdn.microsoft.com/library/windows/hardware/ff569121) | Not applicable | [OID\_WDI\_SET\_ADD\_CIPHER\_KEYS](https://msdn.microsoft.com/library/windows/hardware/dn925855) |
| [OID\_DOT11\_CONNECT\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569122) | Not applicable | [OID\_WDI\_SET\_PRIVACY\_EXEMPTION\_LIST](https://msdn.microsoft.com/library/windows/hardware/dn925940), [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_CURRENT\_PHY\_ID](https://msdn.microsoft.com/library/windows/hardware/ff569135) | Handled by Microsoft | Handled by Microsoft |  |
| [OID\_DOT11\_DESIRED\_BSS\_TYPE](https://msdn.microsoft.com/library/windows/hardware/ff569142) | Handled by Microsoft | Handled by Microsoft |  |
| [OID\_DOT11\_DESIRED\_BSSID\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569141) | Handled by Microsoft | Handled by Microsoft |  |
| [OID\_DOT11\_DESIRED\_COUNTRY\_OR\_REGION\_STRING](https://msdn.microsoft.com/library/windows/hardware/ff569143) | Unsupported | Unsupported |  |
| [OID\_DOT11\_DESIRED\_PHY\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569144) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_DESIRED\_SSID\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569145) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_DISCONNECT\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569147) | Not applicable | [OID\_WDI\_TASK\_DISCONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925951) |
| [OID\_DOT11\_ENABLED\_AUTHENTICATION\_ALGORITHM](https://msdn.microsoft.com/library/windows/hardware/ff569356) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_ENABLED\_MULTICAST\_CIPHER\_ALGORITHM](https://msdn.microsoft.com/library/windows/hardware/ff569357) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_ENABLED\_UNICAST\_CIPHER\_ALGORITHM](https://msdn.microsoft.com/library/windows/hardware/ff569358) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_ENUM\_ASSOCIATION\_INFO](https://msdn.microsoft.com/library/windows/hardware/ff569359) | Handled by Microsoft | Not applicable |
| [OID\_DOT11\_ENUM\_BSS\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569360) | Not applicable | Handled by Microsoft |
| [OID\_DOT11\_EXCLUDE\_UNENCRYPTED](https://msdn.microsoft.com/library/windows/hardware/ff569365) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_EXCLUDED\_MAC\_ADDRESS\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569364) | Handled by Microsoft | Handled by Microsoft |
| [OID\_DOT11\_EXTSTA\_CAPABILITY](https://msdn.microsoft.com/library/windows/hardware/ff569366) | Handled by Microsoft | Not applicable |
| [OID\_DOT11\_FLUSH\_BSS\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569367) | Not applicable | Handled by Microsoft |
| [OID\_DOT11\_HARDWARE\_PHY\_STATE](https://msdn.microsoft.com/library/windows/hardware/ff569370) | Handled by Microsoft | Not applicable |
| [OID\_DOT11\_HIDDEN\_NETWORK\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569371) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_IBSS\_PARAMS](https://msdn.microsoft.com/library/windows/hardware/ff569378) | **No planned support** |  |
| [OID\_DOT11\_MEDIA\_STREAMING\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569386) | Handled by Microsoft | [OID\_WDI\_SET\_CONNECTION\_QUALITY](https://msdn.microsoft.com/library/windows/hardware/dn925927) |
| [OID\_DOT11\_PMKID\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569400) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_PORT\_STATE\_NOTIFICATION](https://msdn.microsoft.com/library/windows/hardware/ff569401) | Not applicable | Unsupported |
| [OID\_DOT11\_POWER\_MGMT\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569402) | Handled by Microsoft | [OID\_WDI\_SET\_CONNECTION\_QUALITY](https://msdn.microsoft.com/library/windows/hardware/dn925927) |
| [OID\_DOT11\_PRIVACY\_EXEMPTION\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569404) | Not applicable | [OID\_WDI\_SET\_PRIVACY\_EXEMPTION\_LIST](https://msdn.microsoft.com/library/windows/hardware/dn925940) |
| [OID\_DOT11\_QOS\_PARAMS](https://msdn.microsoft.com/library/windows/hardware/ff569405) | Handled by Microsoft | Handled by Microsoft |
| [OID\_DOT11\_SAFE\_MODE\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569412) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_STATISTICS](https://msdn.microsoft.com/library/windows/hardware/ff569420) | [OID\_WDI\_GET\_STATISTICS](https://msdn.microsoft.com/library/windows/hardware/dn925850) | Not applicable |
| [OID\_DOT11\_SUPPORTED\_COUNTRY\_OR\_REGION\_STRING](https://msdn.microsoft.com/library/windows/hardware/ff569421) | Unsupported | Not applicable |
| [OID\_DOT11\_SUPPORTED\_MULTICAST\_ALGORITHM\_PAIR](https://msdn.microsoft.com/library/windows/hardware/ff569424) | Handled by Microsoft |  |
| [OID\_DOT11\_SUPPORTED\_UNICAST\_ALGORITHM\_PAIR](https://msdn.microsoft.com/library/windows/hardware/ff569430) | Handled by Microsoft |  |
| [OID\_DOT11\_UNICAST\_USE\_GROUP\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569433) | Handled by Microsoft | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_UNREACHABLE\_DETECTION\_THRESHOLD](https://msdn.microsoft.com/library/windows/hardware/ff569434) | Unsupported | Unsupported |
| *ExtAP* |
| [OID\_DOT11\_ADDITIONAL\_IE](https://msdn.microsoft.com/library/windows/hardware/ff569103) | **No planned support** |  |
| [OID\_DOT11\_AVAILABLE\_CHANNEL\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569107) | **No planned support** |  |
| [OID\_DOT11\_AVAILABLE\_FREQUENCY\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569108) | **No planned support** |  |
| [OID\_DOT11\_DISASSOCIATE\_PEER\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569146) | Not applicable | [OID\_WDI\_TASK\_DISCONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925951) |
| [OID\_DOT11\_ENUM\_PEER\_INFO](https://msdn.microsoft.com/library/windows/hardware/ff569361) | **No planned support** |  |
| [OID\_DOT11\_INCOMING\_ASSOCIATION\_DECISION](https://msdn.microsoft.com/library/windows/hardware/ff569379) | Not applicable | [OID\_WDI\_TASK\_SEND\_AP\_ASSOCIATION\_RESPONSE](https://msdn.microsoft.com/library/windows/hardware/dn925960) |
| [OID\_DOT11\_START\_AP\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/ff569418) | Not applicable | [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_WPS\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/ff569436) | Handled by Microsoft | Handled by Microsoft |
| *Wi-Fi Direct* |
| [OID\_DOT11\_WFD\_ADDITIONAL\_IE](https://msdn.microsoft.com/library/windows/hardware/hh451790) | Not applicable | [OID\_WDI\_SET\_ADVERTISEMENT\_INFORMATION](https://msdn.microsoft.com/library/windows/hardware/dn925860) |
| [OID\_DOT11\_WFD\_CONNECT\_TO\_GROUP\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh464154) | Not applicable | [OID\_WDI\_SET\_PRIVACY\_EXEMPTION\_LIST](https://msdn.microsoft.com/library/windows/hardware/dn925940), [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) |
| [OID\_DOT11\_WFD\_DESIRED\_GROUP\_ID](https://msdn.microsoft.com/library/windows/hardware/hh451791) | Not applicable | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) / [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_WFD\_DEVICE\_CAPABILITY](https://msdn.microsoft.com/library/windows/hardware/hh451792) | Not applicable | [OID\_WDI\_SET\_ADVERTISEMENT\_INFORMATION](https://msdn.microsoft.com/library/windows/hardware/dn925860) |
| [OID\_DOT11\_WFD\_DEVICE\_INFO](https://msdn.microsoft.com/library/windows/hardware/hh451793) | Not applicable | [OID\_WDI\_SET\_ADVERTISEMENT\_INFORMATION](https://msdn.microsoft.com/library/windows/hardware/dn925860) |
| [OID\_DOT11\_WFD\_DEVICE\_LISTEN\_CHANNEL](https://msdn.microsoft.com/library/windows/hardware/hh738803) | Not applicable | Unsupported |
| [OID\_DOT11\_WFD\_DISCONNECT\_FROM\_GROUP\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh451794) | Not applicable | [OID\_WDI\_TASK\_DISCONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925951) |
| [OID\_DOT11\_WFD\_DISCOVER\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh451795) | Not applicable | [OID\_WDI\_TASK\_P2P\_DISCOVER](https://msdn.microsoft.com/library/windows/hardware/dn925955) |
| [OID\_DOT11\_WFD\_ENUM\_DEVICE\_LIST](https://msdn.microsoft.com/library/windows/hardware/hh451796) | Not applicable | Handled by Microsoft |
| [OID\_DOT11\_WFD\_FLUSH\_DEVICE\_LIST](https://msdn.microsoft.com/library/windows/hardware/hh451797) | Not applicable | Handled by Microsoft |
| [OID\_DOT11\_WFD\_GET\_DIALOG\_TOKEN](https://msdn.microsoft.com/library/windows/hardware/hh451798) | Not applicable | Handled by Microsoft |
| [OID\_DOT11\_WFD\_GROUP\_JOIN\_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/hh464155) | Not applicable | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) / [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_WFD\_GROUP\_OWNER\_CAPABILITY](https://msdn.microsoft.com/library/windows/hardware/hh451799) | Not applicable | [OID\_WDI\_SET\_ADVERTISEMENT\_INFORMATION](https://msdn.microsoft.com/library/windows/hardware/dn925860) |
| [OID\_DOT11\_WFD\_GROUP\_START\_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/hh451800) | Not applicable | Saved and set with [OID\_WDI\_TASK\_CONNECT](https://msdn.microsoft.com/library/windows/hardware/dn925948) / [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_WFD\_LISTEN\_STATE\_DISCOVERABILITY](https://msdn.microsoft.com/library/windows/hardware/hh451801) | Not applicable | [OID\_WDI\_SET\_P2P\_LISTEN\_STATE](https://msdn.microsoft.com/library/windows/hardware/dn925935) |
| [OID\_DOT11\_WFD\_SECONDARY\_DEVICE\_TYPE\_LIST](https://msdn.microsoft.com/library/windows/hardware/hh451802) | Not applicable | [OID\_WDI\_SET\_ADVERTISEMENT\_INFORMATION](https://msdn.microsoft.com/library/windows/hardware/dn925860) |
| [OID\_DOT11\_WFD\_SEND\_GO\_NEGOTIATION\_CONFIRMATION](https://msdn.microsoft.com/library/windows/hardware/hh451803) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_RESPONSE\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925957) |
| [OID\_DOT11\_WFD\_SEND\_GO\_NEGOTIATION\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh451804) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_REQUEST\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925956) |
| [OID\_DOT11\_WFD\_SEND\_GO\_NEGOTIATION\_RESPONSE](https://msdn.microsoft.com/library/windows/hardware/hh451805) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_RESPONSE\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925957) |
| [OID\_DOT11\_WFD\_SEND\_INVITATION\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh451806) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_REQUEST\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925956) |
| [OID\_DOT11\_WFD\_SEND\_INVITATION\_RESPONSE](https://msdn.microsoft.com/library/windows/hardware/hh451807) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_RESPONSE\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925957) |
| [OID\_DOT11\_WFD\_SEND\_PROVISION\_DISCOVERY\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh464156) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_REQUEST\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925956) |
| [OID\_DOT11\_WFD\_SEND\_PROVISION\_DISCOVERY\_RESPONSE](https://msdn.microsoft.com/library/windows/hardware/hh451808) | Not applicable | [OID\_WDI\_TASK\_P2P\_SEND\_RESPONSE\_ACTION\_FRAME](https://msdn.microsoft.com/library/windows/hardware/dn925957) |
| [OID\_DOT11\_WFD\_START\_GO\_REQUEST](https://msdn.microsoft.com/library/windows/hardware/hh451809) | Not applicable | [OID\_WDI\_TASK\_START\_AP](https://msdn.microsoft.com/library/windows/hardware/dn925964) |
| [OID\_DOT11\_WFD\_STOP\_DISCOVERY](https://msdn.microsoft.com/library/windows/hardware/hh738804) | Not applicable | Converts to [OID\_WDI\_ABORT\_TASK](https://msdn.microsoft.com/library/windows/hardware/dn925835) |
| *Wi-Fi Power* |
|[OID\_DOT11\_POWER\_MGMT\_MODE\_AUTO\_ENABLED](https://msdn.microsoft.com/library/windows/hardware/hh451788) | Not applicable | [OID\_WDI\_SET\_CONNECTION\_QUALITY](https://msdn.microsoft.com/library/windows/hardware/dn925927) |
| [OID\_DOT11\_POWER\_MGMT\_MODE\_STATUS](https://msdn.microsoft.com/library/windows/hardware/hh451789) | [WDI\_GET\_AUTO\_POWER\_SAVE](https://msdn.microsoft.com/library/windows/hardware/dn925840) | Not applicable |
| [OID\_DOT11\_OFFLOAD\_NETWORK\_LIST](https://msdn.microsoft.com/library/windows/hardware/hh451787) | Not applicable | [OID\_WDI\_SET\_NETWORK\_LIST\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/dn925933) |
| *NDIS* |
| [OID\_GEN\_CURRENT\_LOOKAHEAD](https://msdn.microsoft.com/library/windows/hardware/ff569574) | Not applicable | Unsupported |
| [OID\_GEN\_CURRENT\_PACKET\_FILTER](https://msdn.microsoft.com/library/windows/hardware/ff569575) | Not applicable | [OID\_WDI\_SET\_RECEIVE\_PACKET\_FILTER](https://msdn.microsoft.com/library/windows/hardware/dn925942) |
| [OID\_GEN\_INTERRUPT\_MODERATION](https://msdn.microsoft.com/library/windows/hardware/ff569590) | Handled by Microsoft | Unsupported |
| [OID\_GEN\_LINK\_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/ff569592) | Not applicable | Unsupported |
| [OID\_GEN\_MAXIMUM\_TOTAL\_SIZE](https://msdn.microsoft.com/library/windows/hardware/ff569601) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_RCV\_OK](https://msdn.microsoft.com/library/windows/hardware/ff569632) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_RECEIVE\_BLOCK\_SIZE](https://msdn.microsoft.com/library/windows/hardware/ff569633) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_RECEIVE\_BUFFER\_SPACE](https://msdn.microsoft.com/library/windows/hardware/ff569634) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_STATISTICS](https://msdn.microsoft.com/library/windows/hardware/ff569640) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_TRANSMIT\_BLOCK\_SIZE](https://msdn.microsoft.com/library/windows/hardware/ff569644) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_TRANSMIT\_BUFFER\_SPACE](https://msdn.microsoft.com/library/windows/hardware/ff569645) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_VENDOR\_DESCRIPTION](https://msdn.microsoft.com/library/windows/hardware/ff569649) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_VENDOR\_DRIVER\_VERSION](https://msdn.microsoft.com/library/windows/hardware/ff569650) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_VENDOR\_ID](https://msdn.microsoft.com/library/windows/hardware/ff569651) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_XMIT\_OK](https://msdn.microsoft.com/library/windows/hardware/ff569656) | Handled by Microsoft | Not applicable |
| [OID\_GEN\_PORT\_AUTHENTICATION\_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/ff569623) | Handled by Microsoft | Not applicable |
| *Ethernet* |
| [OID\_802\_3\_ADD\_MULTICAST\_ADDRESS](https://msdn.microsoft.com/library/windows/hardware/ff569068) | Unsupported | Unsupported |
| [OID\_802\_3\_DELETE\_MULTICAST\_ADDRESS](https://msdn.microsoft.com/library/windows/hardware/ff569070) | Unsupported | Unsupported |
| [OID\_802\_3\_PERMANENT\_ADDRESS](https://msdn.microsoft.com/library/windows/hardware/ff569074) | Handled by Microsoft | Not applicable |
| [OID\_802\_3\_CURRENT\_ADDRESS](https://msdn.microsoft.com/library/windows/hardware/ff569069) | Handled by Microsoft | Not applicable |
| [OID\_802\_3\_MULTICAST\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569073) | Handled by Microsoft | [OID\_WDI\_SET\_MULTICAST\_LIST](https://msdn.microsoft.com/library/windows/hardware/dn925932) |
| [OID\_802\_3\_MAXIMUM\_LIST\_SIZE](https://msdn.microsoft.com/library/windows/hardware/ff569072) | Handled by Microsoft | Not applicable |
| [OID\_802\_3\_MAC\_OPTIONS](https://msdn.microsoft.com/library/windows/hardware/ff569071) | Handled by Microsoft | Not applicable |
| [OID\_802\_3\_RCV\_ERROR\_ALIGNMENT](https://msdn.microsoft.com/en-us/library/windows/hardware/ff569075) | Handled by Microsoft | Not applicable |
| [OID\_802\_3\_XMIT\_ONE\_COLLISION](https://msdn.microsoft.com/en-us/library/windows/hardware/ff569082) | Handled by Microsoft | Not applicable |
| [OID\_802\_3\_XMIT\_MORE\_COLLISIONS](https://msdn.microsoft.com/en-us/library/windows/hardware/ff569081) | Handled by Microsoft | Not applicable |
| *NDIS Power* |
| [OID\_PNP\_QUERY\_POWER](https://msdn.microsoft.com/library/windows/hardware/ff569778) | Handled by Microsoft | Not applicable |
| [OID\_PNP\_SET\_POWER](https://msdn.microsoft.com/library/windows/hardware/ff569780) | Not applicable | [OID\_WDI\_SET\_POWER\_STATE](https://msdn.microsoft.com/library/windows/hardware/dn925939), [OID\_WDI\_SET\_NETWORK\_LIST\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/dn925933), [OID\_WDI\_TASK\_OPEN](https://msdn.microsoft.com/library/windows/hardware/dn925954) (hibernate), [OID\_WDI\_TASK\_CLOSE](https://msdn.microsoft.com/library/windows/hardware/dn925947) (hibernate) |
| [OID\_PM\_ADD\_PROTOCOL\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/ff569763) | Not applicable | [OID\_WDI\_SET\_ADD\_PM\_PROTOCOL\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/dn925857) |
| [OID\_PM\_ADD\_WOL\_PATTERN](https://msdn.microsoft.com/library/windows/hardware/ff569764) | Not applicable | [OID\_WDI\_SET\_ADD\_WOL\_PATTERN](https://msdn.microsoft.com/library/windows/hardware/dn925858) |
| [OID\_PM\_CURRENT\_CAPABILITIES](https://msdn.microsoft.com/library/windows/hardware/ff569765) | Handled by Microsoft |  |
| [OID\_PM\_GET\_PROTOCOL\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/ff569766) | Not applicable | [OID\_WDI\_GET\_PM\_PROTOCOL\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/dn925846) |
| [OID\_PM\_HARDWARE\_CAPABILITIES](https://msdn.microsoft.com/library/windows/hardware/ff569767) | Handled by Microsoft | Not applicable |
| [OID\_PM\_PARAMETERS](https://msdn.microsoft.com/library/windows/hardware/ff569768) | Handled by Microsoft | Handled by Microsoft |
| [OID\_PM\_PROTOCOL\_OFFLOAD\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569769) | Handled by Microsoft | Not applicable |
| [OID\_PM\_REMOVE\_PROTOCOL\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/ff569770) | Not applicable | [OID\_WDI\_SET\_REMOVE\_PM\_PROTOCOL\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/dn925943) |
| [OID\_PM\_REMOVE\_WOL\_PATTERN](https://msdn.microsoft.com/library/windows/hardware/ff569771) | Not applicable | [OID\_WDI\_SET\_REMOVE\_WOL\_PATTERN](https://msdn.microsoft.com/library/windows/hardware/dn925944) |
| [OID\_PM\_WOL\_PATTERN\_LIST](https://msdn.microsoft.com/library/windows/hardware/ff569772) | Handled by Microsoft | Not applicable |
| [OID\_PACKET\_COALESCING\_FILTER\_MATCH\_COUNT](https://msdn.microsoft.com/library/windows/hardware/hh451826) | [WDI\_GET\_RECEIVE\_ COALESCING\_MATCH\_COUNT](https://msdn.microsoft.com/library/windows/hardware/dn925848) | Not applicable |
| [OID\_RECEIVE\_FILTER\_SET\_FILTER](https://msdn.microsoft.com/library/windows/hardware/ff569795) | Not applicable | [OID\_WDI\_SET\_RECEIVE\_COALESCING](https://msdn.microsoft.com/library/windows/hardware/dn925941) |
| [OID\_RECEIVE\_FILTER\_CLEAR\_FILTER](https://msdn.microsoft.com/library/windows/hardware/ff569785) | Not applicable | [OID\_WDI\_SET\_CLEAR\_RECEIVE\_COALESCING](https://msdn.microsoft.com/library/windows/hardware/dn925926) |
| *TCP Task Offload* |
| [OID\_TCP\_TASK\_OFFLOAD](https://msdn.microsoft.com/library/windows/hardware/ff569815) | Unsupported | Unsupported |

 

 

 





