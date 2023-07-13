Актуальний Rea_me excel файлл є в попередній версії програми 
# LEPS_3-Basic-LEPS_4-Basic-LEPS_4-Virt_Int---Harnesses_to_Internal_and_check___V2

LEPS_3_Basic

Програма створена для генерації Internal_module під вязки, а також перевіряє генерацію по певним пунктам.						
Друга функція програми порівнює проводи під згенеровані Internal модулі з проводами згідно кастомер модулів з Wirelist (тобто чи замовились правильні проводи під вязки).						
						
Критерії перевірки першої функції:						
The_same_index_in_one_Internal - прописаний один індекс два рази під один інтернал						
Different_names_in_Basic_Module_and_Scan_Code - різні назви в колонках Basic_Module та Scan_Code						
The_same_name_Internal_module_in_different_group - назва інтернал модуля повторюється в різних групах						
Ordered_more_than_one_index_prescribed_as_OR - замовився більше одного індексу прописаних через "або"						
More_than_one_internal_in_one_group - замовились два продукційні модулі з одної групи						
Index_are_in_Harnesses_but_absent_in_Basic_Module - індекс є у вязці але відсутній у мастердаті						
Unrealized_index - індекс заказався але не реалізувався в групі						
Критерії перевірки другої функції:						
Duplicate_of_wires_in_internal - замовились два однакові проводи в продукційних модулях						
Duplicate_of_wires_in_Wirelist - замовились два однакові проводи в Wirelist (теоретично така помилка неможлива(тільки у випадку якшо помилка у файлику))						
Is_in_Wirelist_absent_in_Internal - проводи замовились згідно кастомер модулів і Wirelist, але відсутні у продукційних модулях						
Is_in_Internal_absent_in_Wirelist - проводи замовились згідно продукційних модулів але відсутні згідно Wirelist і кастомемр модулів						
						
Всі файлики повинні бути формату - csv						
Стандарт Basic_Module:						
Basic_Module	Module	[Index]	Basic_Module_Group	ScanCode	Enable_Print	Enable_PIC
2000P01PV02	236B380HC	1	1	2000P01PV02	1	0
2000P01PV02	236BA673C	1	1	2000P01PV02	1	0
2000P01PV02	236BA663C	1	1	2000P01PV02	1	0
2000P45PV01	236B380HC	1	2	2000P45PV01	1	0
2000P45PV01	236BA673C	1	2	2000P45PV01	1	0
2000P46PV01	236BA663C	1	2	2000P46PV01	1	0
2000P03PV01	236B380HC	1	3	2000P03PV01	1	0
2000P03PV01	236BA663C	1	3	2000P03PV01	1	0
						
						
Стандарт Wirelist:						
Ltg,Nr,	Index	Variante	Variant			
7876_1	91S03670A	A 254 540 02 31	V156			
7876_2	91S03670A	A 254 540 02 31	V156			
7899_1	91S03730A	A 254 540 04 31	V936			
7899_2	91S03730A	A 254 540 04 31	V936			
7902_1	91S03730A	A 254 540 04 31	V936			
1433_1	91S03660A	A 254 540 20 31	V72			
1433_2	91S03660A	A 254 540 20 31	V72			
6359	91S03680A	A 254 540 52 30	V709			
6360	91S03680A	A 254 540 52 30	V709	останні два стовпці не обовязкові (для інформації)		
						
Стандарт Wires_in_prod_modules:						
WIRE	PM					
1007	99P01XLV1					
1008	99P01XLV1					
1013	9323P01XLV1					
1014	9323P01XLV1					
1025	92P03XLV1					
1026	92P03XLV1					
1027	92P03XLV1					
1036	91F010XLV2					
1042	91F010XLV2					
1043	91F010XLV2					
						
						
						
Стандарт harnesses (Вязки можуть бути розбиті по декільком файлам):						
Customer JIT Call Number	Customer material number	Comp. Group Material	JIT call quantity	Material		
9418259	91N0001	X254LRB	1	91K02170A	PDC-D	
9418259	91N0002	X254LRB	1	91K02180A	PDC-P	
9418259	91M0622	X254LRB	1	91K02200A	PDC-R Medium	
9418259	91Y0216	X254LRB	1	91S00010A	Cable channel	
9418259	91M0623	X254LRB	1	91S00070A	MFB-R	
9418259	91M0630	X254LRB	1	91S00120A	brokenconnector 3	
9418259	91M0628	X254LRB	1	91S00140A	brokenconnector 1	
9418259	91Y0498	X254LRB	1	91S00160B	V16	
9418259	91Y0538	X254LRB	1	91S00190B	V40	другий, третій, четвертий, шостий стовпці не обовязкові (формат взятий з мейлів від FST)
![Uploading image.png…]()




LEPS_4_Basic
Програма створена для генерації Internal_module під вязки, а також перевіряє генерацію по певним пунктам.						
Друга функція програми порівнює проводи під згенеровані Internal модулі з проводами згідно кастомер модулів з Wirelist (тобто чи замовились правильні проводи під вязки).						
						
Критерії перевірки першої функції:						
The_same_index_in_one_Internal - прописаний один індекс два рази під один інтернал						
The_same_name_Internal_module_in_different_group - назва інтернал модуля повторюється в різних групах						
Ordered_more_than_one_index_prescribed_as_OR - замовився більше одного індексу прописаних через "або"						
More_than_one_internal_in_one_group - замовились два продукційні модулі з одної групи						
Index_are_in_Harnesses_but_absent_in_Basic_Module - індекс є у вязці але відсутній у мастердаті						
Unrealized_index - індекс заказався але не реалізувався в групі						
Критерії перевірки другої функції:						
Duplicate_of_wires_in_internal - замовились два однакові проводи в продукційних модулях						
Duplicate_of_wires_in_Wirelist - замовились два однакові проводи в Wirelist (теоретично така помилка неможлива(тільки у випадку якшо помилка у файлику))						
Is_in_Wirelist_absent_in_Internal - проводи замовились згідно кастомер модулів і Wirelist, але відсутні у продукційних модулях						
Is_in_Internal_absent_in_Wirelist - проводи замовились згідно продукційних модулів але відсутні згідно Wirelist і кастомемр модулів						
						
Всі файлики повинні бути формату - csv						
Стандарт Basic_Module:						
BasicModuleNumber	BasicModuleGroup	ModuleIndex	ModuleNumber			
2000P01PV02	1	1	236B380HD			
2000P01PV02	1	1	236BA673D			
2000P01PV02	1	1	236BA663D			
2000P45PV01	2	1	236B380HD			
2000P45PV01	2	1	236BA673D			
2000P46PV01	2	1	236BA663D			
2000P03PV01	3	1	236B380HD			
2000P03PV01	3	1	236BA663D			
2000P29PV01	3	1	236BA673D			
2000P20PV01	3	1	236B380HD			
2000P20PV01	3	2	236B520EA			
						
Стандарт Wirelist:						
Ltg,Nr,	Index	Variante	Variant			
7876_1	91S03670A	A 254 540 02 31	V156			
7876_2	91S03670A	A 254 540 02 31	V156			
7899_1	91S03730A	A 254 540 04 31	V936			
7899_2	91S03730A	A 254 540 04 31	V936			
7902_1	91S03730A	A 254 540 04 31	V936			
1433_1	91S03660A	A 254 540 20 31	V72			
1433_2	91S03660A	A 254 540 20 31	V72			
6359	91S03680A	A 254 540 52 30	V709			
6360	91S03680A	A 254 540 52 30	V709	останні два стовпці не обовязкові (для інформації)		
						
Стандарт Wires_in_prod_modules:						
WIRE	PM					
1007	99P01XLV1					
1008	99P01XLV1					
1013	9323P01XLV1					
1014	9323P01XLV1					
1025	92P03XLV1					
1026	92P03XLV1					
1027	92P03XLV1					
1036	91F010XLV2					
1042	91F010XLV2					
1043	91F010XLV2					
						
						
						
Стандарт harnesses (Вязки можуть бути розбиті по декільком файлам):						
Customer JIT Call Number	Customer material number	Comp. Group Material	JIT call quantity	Material		
9418259	91N0001	X254LRB	1	91K02170A	PDC-D	
9418259	91N0002	X254LRB	1	91K02180A	PDC-P	
9418259	91M0622	X254LRB	1	91K02200A	PDC-R Medium	
9418259	91Y0216	X254LRB	1	91S00010A	Cable channel	
9418259	91M0623	X254LRB	1	91S00070A	MFB-R	
9418259	91M0630	X254LRB	1	91S00120A	brokenconnector 3	
9418259	91M0628	X254LRB	1	91S00140A	brokenconnector 1	
9418259	91Y0498	X254LRB	1	91S00160B	V16	
9418259	91Y0538	X254LRB	1	91S00190B	V40	другий, третій, четвертий, шостий стовпці не обовязкові (формат взятий з мейлів від FST)
![Uploading image.png…]()






LEPS_4_Virtual_Internal

Програма створена для генерації Internal_module під вязки, а також перевіряє генерацію по певним пунктам.						
Друга функція програми порівнює проводи під згенеровані Internal модулі з проводами згідно кастомер модулів з Wirelist (тобто чи замовились правильні проводи під вязки).						
						
Критерії перевірки першої функції:						
The_same_name_Internal_module_in_different_group - назва інтернал модуля повторюється в різних групах						
Ordered_more_than_one_index_for_one_Virtual - замовився більше одного індексу прописаних через "або", тобто більше одного індексу на один віртуал						
No_index_in_virtual_master_data - відсутні індекси у Virtual						
More_than_one_internal_in_one_group - замовились два продукційні модулі з одної групи						
Unrealized_Virtual_module - віртуал модуль заказався під індекс але не реалізований в групі						
Критерії перевірки другої функції:						
Duplicate_of_wires_in_internal - замовились два однакові проводи в продукційних модулях						
Duplicate_of_wires_in_Wirelist - замовились два однакові проводи в Wirelist (теоретично така помилка неможлива(тільки у випадку якшо помилка у файлику))						
Is_in_Wirelist_absent_in_Internal - проводи замовились згідно кастомер модулів і Wirelist, але відсутні у продукційних модулях						
Is_in_Internal_absent_in_Wirelist - проводи замовились згідно продукційних модулів але відсутні згідно Wirelist і кастомемр модулів						
						
Всі файлики повинні бути формату - csv						
Стандарт Internal:						
InternalModuleNumber	InternalModuleGroup	ModuleNumber	OrderType			
PP00840846	XLA009	LF1_XLA009	X254L%			
9328F01XLV1	XLF001	V328_XLF001	X254L%			
9218F01XLV1	XLF003	V218_XLF003	X254L%			
91F038XLV1	XLF004	V1_V1D_XLF004	X254L%			
91F041XLV1	XLF004	V1_V1D_XLF004	X254L%			
91F041XLV1	XLF004	V740_XLF004	X254L%			
91F045XLV1	XLF004	V1_V1D_XLF004	X254L%			
91F045XLV1	XLF004	V712_V713_V712B_V713C_XLF004	X254L%			
						
Стандарт Virtual:						
VirtualModuleNumber	ModuleNumber	OrderType				
LF1_XLA009	91S03230B	X254L%				
V328_XLF001	91S01600C	X254L%				
V218_XLF003	91S01430D	X254L%				
V1_V1D_XLF004	91S00540J	X254L%				
V1_V1D_XLF004	91S03600B	X254L%				
V740_XLF004	91S02050B	X254L%				
V712_V713_V712B_V713C_XLF004	91S03080G	X254L%				
V712_V713_V712B_V713C_XLF004	91S01890F	X254L%				
						
Стандарт Wirelist:						
Ltg,Nr,	Index	Variante	Variant			
7876_1	91S03670A	A 254 540 02 31	V156			
7876_2	91S03670A	A 254 540 02 31	V156			
7899_1	91S03730A	A 254 540 04 31	V936			
7899_2	91S03730A	A 254 540 04 31	V936			
7902_1	91S03730A	A 254 540 04 31	V936			
1433_1	91S03660A	A 254 540 20 31	V72			
1433_2	91S03660A	A 254 540 20 31	V72			
6359	91S03680A	A 254 540 52 30	V709			
6360	91S03680A	A 254 540 52 30	V709	останні два стовпці не обовязкові (для інформації)		
						
Стандарт Wires_in_prod_modules:						
WIRE	PM					
1007	99P01XLV1					
1008	99P01XLV1					
1013	9323P01XLV1					
1014	9323P01XLV1					
1025	92P03XLV1					
1026	92P03XLV1					
1027	92P03XLV1					
1036	91F010XLV2					
1042	91F010XLV2					
1043	91F010XLV2					
						
						
						
Стандарт harnesses (Вязки можуть бути розбиті по декільком файлам):						
Customer JIT Call Number	Customer material number	Comp. Group Material	JIT call quantity	Material		
9418259	91N0001	X254LRB	1	91K02170A	PDC-D	
9418259	91N0002	X254LRB	1	91K02180A	PDC-P	
9418259	91M0622	X254LRB	1	91K02200A	PDC-R Medium	
9418259	91Y0216	X254LRB	1	91S00010A	Cable channel	
9418259	91M0623	X254LRB	1	91S00070A	MFB-R	
9418259	91M0630	X254LRB	1	91S00120A	brokenconnector 3	
9418259	91M0628	X254LRB	1	91S00140A	brokenconnector 1	
9418259	91Y0498	X254LRB	1	91S00160B	V16	
9418259	91Y0538	X254LRB	1	91S00190B	V40	другий, четвертий, шостий стовпці не обовязкові (формат взятий з мейлів від FST)
![Uploading image.png…]()
