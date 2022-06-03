- 1.2-CL-3541083
```c++ 
Free "48 8B 01 48 8B D3 FF 50 20 48 83 C4 20 5B" 
```

- 1.8-CL-3724489
```c++
GEngineOffset 			=	0x674AB20;		//Global Engine*
GWorldOffset				=	0x674CD00;		//Global World*
GNamesOffset 				=	0x66587C8;		//Global NameArray*
GUObjectArrayOffset 		=	0x6661380;		//Global ObjectArray-Class*
TUObjectArrayOffset 		=	0x6661390;		//Global ObjectArray*
ProcessEventOffset 		=	0x13D86E0;		//UObject::ProcessEvent()
SCO_IOffset 				=	0x13DD730;		//StaticContructObject_Internal()
SLO_IOffset 				=	0x13E0180;		//StaticLoadObject_Internal()
SpawnActorOffset 			=	0x137DBC0;		//UWorld::SpawnActor()
PlainNameStringOffset 	=	0x12F0FC0;		//FNameEntry::GetPlainNameString()
CGInternalOffset			=	0x137D380;		//CollectGarbageInternal()
GiveAbilityOffset			=	0x3D50A60;		//GiveAbility()
```

- 1.11-CL-3807424	
```c++
GObjectsPointer = OffsetTable::GObjects = reinterpret_cast<FUObjectArray*>((PBYTE)base_address + 0x5CC1310);
GetObjectNameOffset = OffsetTable::GetObjectName = 0x1A51920;
OffsetTable::ProcessEvent = FindPattern(XORSTRING("\x40\x55\x56\x57\x41\x54\x41\x55\x41\x56\x41\x57\x48\x81\xEC\x00\x00\x00\x00\x48\x8D\x6C\x24\x00\x48\x89\x9D\x00\x00\x00\x00\x48\x8B\x05\x00\x00\x00\x00\x48\x33\xC5\x48\x89\x85\x00\x00\x00\x00\x48\x63\x41\x0C"), XORSTRING("xxxxxxxxxxxxxxx????xxxx?xxx????xxx????xxxxxx????xxxx"));
OffsetTable::UEngine = 0x5DA3F20;
OffsetTable::ViewPort = 0x720;
OffsetTable::World = 0x80;
OffsetTable::GameInstance = 0x88;
OffsetTable::LocalPlayers = 0x38;
OffsetTable::PlayerController = 0x30;
OffsetTable::GameMode = 0xF0;
OffsetTable::GameState = 0xF8;
OffsetTable::MinimapBrush = 0x1438;
OffsetTable::MinimapSecondBrush = 0x0;
OffsetTable::StrongMyHero = 0x31B0;
OffsetTable::CharacterParts = 0x280;
OffsetTable::AdditionalData = 0x530;
OffsetTable::SprintingBool = 0xF85;
OffsetTable::MovementStyle = 0x804;
OffsetTable::MinimapThirdBrush = 0x0;
OffsetTable::MinimapFourthBrush = 0x0;
OffsetTable::MinimapFifthBrush = 0x0;
OffsetTable::MinimapSixthBrush = 0x0;
OffsetTable::MinimapSeventhBrush = 0x0;
OffsetTable::Inventory = 0x1DB8;
OffsetTable::QuickBar = 0x1B10;
OffsetTable::ItemInstances = 0x488;
OffsetTable::ItemEntries = 0x428;
OffsetTable::ItemEntry = 0x1E0;
OffsetTable::SpawnActor = FindPattern(XORSTRING("\xE8\x00\x00\x00\x00\x0F\x10\x04\x37"), XORSTRING("x????xxxx"));
```
- 2.4.2-CL-3870737
```c++
GObjectsPointer = OffsetTable::GObjects = reinterpret_cast<FUObjectArray*>((PBYTE)base_address + 0x44E5CE0);
GetObjectNameOffset = OffsetTable::GetObjectName = 0x1A8B7D0;
OffsetTable::ProcessEvent = FindPattern(XORSTRING("\x40\x55\x56\x57\x41\x54\x41\x55\x41\x56\x41\x57\x48\x81\xEC\x00\x00\x00\x00\x48\x8D\x6C\x24\x00\x48\x89\x9D\x00\x00\x00\x00\x48\x8B\x05\x00\x00\x00\x00\x48\x33\xC5\x48\x89\x85\x00\x00\x00\x00\x48\x63\x41\x0C"), XORSTRING("xxxxxxxxxxxxxxx????xxxx?xxx????xxx????xxxxxx????xxxx"));
OffsetTable::UEngine = 0x45CB8A0;
OffsetTable::ViewPort = 0x720;
OffsetTable::World = 0x80;
OffsetTable::GameInstance = 0x88;
OffsetTable::LocalPlayers = 0x38;
OffsetTable::PlayerController = 0x30;
OffsetTable::GameMode = 0x140;
OffsetTable::GameState = 0x148;
OffsetTable::MinimapBrush = 0x1458;
OffsetTable::MinimapSecondBrush = 0x14E0;
OffsetTable::StrongMyHero = 0x2EB0;
OffsetTable::CharacterParts = 0x280;
OffsetTable::AdditionalData = 0x4F0;
OffsetTable::SprintingBool = 0x1015;
OffsetTable::MovementStyle = 0x814;
OffsetTable::MinimapThirdBrush = 0x0;
OffsetTable::MinimapFourthBrush = 0x0;
OffsetTable::MinimapFifthBrush = 0x0;
OffsetTable::MinimapSixthBrush = 0x0;
OffsetTable::MinimapSeventhBrush = 0x0;
OffsetTable::Inventory = 0x1E18;
OffsetTable::QuickBar = 0x1B70;
OffsetTable::ItemInstances = 0x488;
OffsetTable::ItemEntries = 0x428;
OffsetTable::ItemEntry = 0x1E0;
OffsetTable::SpawnActor = FindPattern(XORSTRING("\xE8\x00\x00\x00\x00\x0F\x10\x04\x3E"), XORSTRING("x????xxxx"));
```
- 2.5.0-CL-3889387
```c++
GOBJECTS _("48 8B 05 ? ? ? ? 48 8D 1C C8 81 4B ? ? ? ? ? 49 63 76 30")
FNAME_TOSTRING _("48 89 5C 24 ? 57 48 83 EC 40 83 79 04 00 48 8B DA 48 8B F9")
GETFIRSTPLAYERCONTROLLER _("83 B9 ? ? ? ? ? 7E ? 48 8B 89 ? ? ? ? E9")
SPAWNACTORFROMCLASS _("40 53 56 57 48 83 EC 70 48 8B 05 ? ? ? ? 48 33 C4 48 89 44 24 ? 0F 28 1D ? ? ? ? 0F 57 D2 48 8B B4 24 ? ? ? ? 0F 28 CB")
CONSTRUCTOBJECT _("4C 89 44 24 ? 53 55 56 57 41 54 41 56 41 57 48 81 EC ? ? ? ? 48 8B 05 ? ? ? ?")
LOADOBJECT _("4C 89 4C 24 ? 48 89 54 24 ? 48 89 4C 24 ? 55 53 56 57 48 8D 6C 24 ? 48 81 EC ? ? ? ? 33 D2")
GETROW _("48 89 5C 24 ? 48 89 74 24 ? 48 89 54 24 ? 57 48 83 EC 60 48 83 79 ? ? 41 0F B6 F9 49 8B F0 48 8B D9 75 6C 80 3D ? ? ? ? ? 0F 82 ? ? ? ? 45 33 C0 48 8D 54 24 ? E8 ? ? ? ? 83 78 08 00 74 05 48 8B 18 EB 07")
FREE _("48 85 C9 74 1D 4C 8B 05 ? ? ? ? 4D 85 C0")

```
- 3.2-CL-3935073
```c++
GObjectsPointer = OffsetTable::GObjects = reinterpret_cast<FUObjectArray*>((PBYTE)base_address + 0x48F72F0);
GetObjectNameOffset = OffsetTable::GetObjectName = 0x210CAC0;
OffsetTable::ProcessEvent = FindPattern(XORSTRING("\x40\x55\x56\x57\x41\x54\x41\x55\x41\x56\x41\x57\x48\x81\xEC\x00\x00\x00\x00\x48\x8D\x6C\x24\x00\x48\x89\x9D\x00\x00\x00\x00\x48\x8B\x05\x00\x00\x00\x00\x48\x33\xC5\x48\x89\x85\x00\x00\x00\x00\x48\x63\x41\x0C"), XORSTRING("xxxxxxxxxxxxxxx????xxxx?xxx????xxx????xxxxxx????xxxx"));
OffsetTable::UEngine = 0x49EF310;
OffsetTable::ViewPort = 0x720;
OffsetTable::World = 0x88;
OffsetTable::GameInstance = 0x90;
OffsetTable::LocalPlayers = 0x38;
OffsetTable::PlayerController = 0x30;
OffsetTable::GameMode = 0x140;
OffsetTable::GameState = 0x148;
OffsetTable::MinimapBrush = 0x15B8;
OffsetTable::MinimapSecondBrush = 0x1660;
OffsetTable::StrongMyHero = 0x2FC0;
OffsetTable::CharacterParts = 0x258;
OffsetTable::AdditionalData = 0x500;
OffsetTable::SprintingBool = 0xFE5;
OffsetTable::MovementStyle = 0x7C4;
OffsetTable::MinimapThirdBrush = 0x16D8;
OffsetTable::MinimapFourthBrush = 0x1750;
OffsetTable::MinimapFifthBrush = 0x17C8;
OffsetTable::MinimapSixthBrush = 0x1840;
OffsetTable::MinimapSeventhBrush = 0x18B8;
OffsetTable::Inventory = 0x1DE8;
OffsetTable::QuickBar = 0x1B48;
OffsetTable::ItemInstances = 0x438;
OffsetTable::ItemEntries = 0x3D8;
OffsetTable::ItemEntry = 0x1E0;
OffsetTable::SpawnActor = FindPattern(XORSTRING("\xE8\x00\x00\x00\x00\x0F\x10\x04\x3E"), XORSTRING("x????xxxx"));
```
- 4.5-CL-4159770 
```c++
GOBJECTS _("48 8B 05 ? ? ? ? 48 8D 1C C8 81 4B ? ? ? ? ? 49 63 76 30")
FNAME_TOSTRING _("48 89 5C 24 ? 57 48 83 EC 40 83 79 04 00 48 8B DA 48 8B F9")
GETFIRSTPLAYERCONTROLLER _("83 B9 ? ? ? ? ? 7E ? 48 8B 89 ? ? ? ? E9")
SPAWNACTORFROMCLASS _("40 53 56 57 48 83 EC 70 48 8B 05 ? ? ? ? 48 33 C4 48 89 44 24 ? 0F 28 1D ? ? ? ? 0F 57 D2 48 8B B4 24 ? ? ? ? 0F 28 CB")
CONSTRUCTOBJECT _("4C 89 44 24 ? 53 55 56 57 41 54 41 56 41 57 48 81 EC ? ? ? ? 48 8B 05 ? ? ? ?")
LOADOBJECT _("4C 89 4C 24 ? 48 89 54 24 ? 48 89 4C 24 ? 55 53 56 57 48 8D 6C 24 ? 48 81 EC ? ? ? ? 33 D2")
GETROW _("48 89 5C 24 ? 48 89 74 24 ? 48 89 54 24 ? 57 48 83 EC 60 48 83 79 ? ? 41 0F B6 F9 49 8B F0 48 8B D9 75 6C 80 3D ? ? ? ? ? 0F 82 ? ? ? ? 45 33 C0 48 8D 54 24 ? E8 ? ? ? ? 83 78 08 00 74 05 48 8B 18 EB 07")
FREE _("48 85 C9 74 1D 4C 8B 05 ? ? ? ? 4D 85 C0")
```
- 5-6
```c++
GOBJECTS _("48 8B 05 ? ? ? ? 48 8B 0C C8 48 8D 04 D1 EB 03 48 8B ? 81 48 08 ? ? ? 40 49")
FNAME_TOSTRING _("48 89 5C 24 ? 57 48 83 EC 30 83 79 04 00 48 8B DA 48 8B F9")
GETFIRSTPLAYERCONTROLLER _("83 B9 ? ? ? ? ? 7E ? 48 8B 89 ? ? ? ? E9")
SPAWNACTORFROMCLASS _("40 53 56 57 48 83 EC 70 48 8B 05 ? ? ? ? 48 33 C4 48 89 44 24 ? 0F 28 1D ? ? ? ? 0F 57 D2 48 8B B4 24 ? ? ? ? 0F 28 CB")
CONSTRUCTOBJECT _("48 89 5C 24 ? 55 56 57 41 54 41 55 41 56 41 57 48 8D AC 24 ? ? ? ? 48 81 EC ? ? ? ? 48 8B 05 ? ? ? ? 48 33 C4 48 89 85 ? ? ? ? 44 8B A5 ? ? ? ? 48 8D 05 ? ? ? ?")
LOADOBJECT _("4C 89 4C 24 ? 48 89 54 24 ? 48 89 4C 24 ? 55 53 56 57 41 54 41 55 41 56 41 57 48 8B EC 48 83 EC 78 45 33 F6")
FREE _("48 85 C9 74 2E 53 48 83 EC 20 48 8B D9")
```
- 7.30-CL-4834550 `+ 7.4`

```c++
GOBJECTS _("48 8B 05 ? ? ? ? 48 8B 0C C8 48 8D 04 D1 EB 03 48 8B ? 81 48 08 ? ? ? 40 49")
FNAME_TOSTRING _("48 89 5C 24 ? 57 48 83 EC 30 83 79 04 00 48 8B DA 48 8B F9")
GETFIRSTPLAYERCONTROLLER _("83 B9 ? ? ? ? ? 7E ? 48 8B 89 ? ? ? ? E9")
SPAWNACTORFROMCLASS _("40 53 56 57 48 83 EC 70 48 8B 05 ? ? ? ? 48 33 C4 48 89 44 24 ? 0F 28 1D ? ? ? ? 0F 57 D2 48 8B B4 24 ? ? ? ? 0F 28 CB")
CONSTRUCTOBJECT _("48 89 5C 24 ? 55 56 57 41 54 41 55 41 56 41 57 48 8D AC 24 ? ? ? ? 48 81 EC ? ? ? ? 48 8B 05 ? ? ? ? 48 33 C4 48 89 85 ? ? ? ? 44 8B A5 ? ? ? ? 48 8D 05 ? ? ? ?")
LOADOBJECT _("4C 89 4C 24 ? 48 89 54 24 ? 48 89 4C 24 ? 55 53 56 57 41 54 41 55 41 56 41 57 48 8B EC 48 83 EC 78 45 33 F6")
FREE _("48 85 C9 74 2E 53 48 83 EC 20 48 8B D9")
```
- 8.40-CL-6005771
```c++
GOBJECTS _("48 8B 05 ? ? ? ? 48 8B 0C C8 48 8D 04 D1 EB 03 48 8B ? 81 48 08 ? ? ? 40 49")
FNAME_TOSTRING _("48 89 5C 24 ? 57 48 83 EC 30 83 79 04 00 48 8B DA 48 8B F9")
GETFIRSTPLAYERCONTROLLER _("83 B9 ? ? ? ? ? 7E ? 48 8B 89 ? ? ? ? E9")
SPAWNACTORFROMCLASS _("40 53 56 57 48 83 EC 70 48 8B 05 ? ? ? ? 48 33 C4 48 89 44 24 ? 0F 28 1D ? ? ? ? 0F 57 D2 48 8B B4 24 ? ? ? ? 0F 28 CB")
CONSTRUCTOBJECT _("48 89 5C 24 ? 55 56 57 41 54 41 55 41 56 41 57 48 8D AC 24 ? ? ? ? 48 81 EC ? ? ? ? 48 8B 05 ? ? ? ? 48 33 C4 48 89 85 ? ? ? ? 44 8B A5 ? ? ? ? 48 8D 05 ? ? ? ?")
LOADOBJECT _("4C 89 4C 24 ? 48 89 54 24 ? 48 89 4C 24 ? 55 53 56 57 41 54 41 55 41 56 41 57 48 8B EC 48 83 EC 78 45 33 F6")
FREE _("48 85 C9 74 2E 53 48 83 EC 20 48 8B D9")
```


