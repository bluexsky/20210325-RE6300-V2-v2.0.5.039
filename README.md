# RE6300-V2-v2.0.5.039

Firmware Version:

2.0.05.039 (RC6)
2.0.05.008 (RC5)
Competitor
Linksys	RE6300v1
Netgear	EX3700
AC750 product
2.4 GHz Radio
Vendor	MTK
Chip	MT7603e
MIMO	2x2:2
Link Speed

300 Mbps (11n)

5 GHz Radio
Vendor	MTK
Chip	MT7663
MIMO	1x1
Link Speed	
433Mbps (11ac)

RE6300v2 (Jarvis) is a cost down version of existing RE6300v1 (N300 + AC433) + 1G ethernet port.

ODM of RE6300v2 is GEMTEK.

Project page: https://wiki.belkin.com/pages/viewpage.action?pageId=121266596

JIRA Project: https://jira.belkin.com/browse/GEMTEK , JIRA component: RE6300V2-Jarvis

Rework and double check console connection before plug in AC

Please firstly be sure to check the console as following before plug in AC power.  

The red line should be cut by ODM to avoid burning.

The correct situation should be:





And Rework is needed if current fw version is older than 2.0.04(included):

Because Jarvis converted firmware image header since version 2.0.05, so all of
firmware before 2.0.04(included) needed to do firmware migration flow, then Jarvis
can use 2.0.05(after).

SOP file: Jarvis Firmware version migrate information.pdf

Image file needed for SOP: JARVIS-noHeaderCheck.img



Open JIRA Issues Reported by/Assigned to Irvine QA - https://jira.belkin.com/browse/GEMTEK
键值	摘要	T	已创建的	已更新	到期	经办人	报告人	P	状态	解决结果找不到问题  刷新
2.0.05.039 (RC6)
In this RC6, the wifi performance spec is turned to AC750 , please adjust pass/fail criteria accordingly.

Start Date	End Date	Tester	Result	Competitors	Summary
Sanity Test

3/15/21	3/22/21	
Eun

RE6300v2_2.0.05.039_Sanity.xlsx



Duration	3/15/21	TBD	Eun	
2021-3-22  Added to Duration1 TestBed. AP mode.

running 0 days as of2021-3-22


No issue.
Chamber (RE)	3/15/21	3/19/21	Eric	
RE6300v2_2.0.05.039_RE.xlsx

RE6400

No issues
Test House (RE)	3/15/21	3/19/21	
Dominic

use E7350 as root AP

RE6300v2_2.0.05.039 (RC6)_TH_RE_Comp.xlsx

RE6300v1

Comparing to previous FW (RC5):

Throughput Rate: The following TPs have lower rate:
Crossband: TP3(all dir)
NonCrossband: TP3(Down/Up), X2: TP3(Up/Bidir),
Number of Rerun:  3 - 5 times @TP3Rate is lower @TP3
Special Remark: Rate is lower than expected @TP3 fro Crossband mode
