Teko lena ha Nitro 1 month ka 50 me ?
#define GNames_Offset  0x4affd94
#define GUobject_Offset 0xa0afcb8
#define Process_Event_Offset 0x65a9cac
#define Process_Event_Skins 0x4d92af4
#define GNativeApp_Offset 0x9ef7638
#define GetActorArray_Offset 0x6a45788
#define Strlen_Offset 0x90a5650
#define ShootEvent_Offset 0x358146c
#define Unlock_120_Fps_Offset 0x358146c
#define Open_All_Drawings_Offset 0x31107f0
#define Lobby_Skin_Player_Offset 0x36ea734
#define eglSwapBuffers  0x711ce4c
Actors_Offset : 0x70
static auto aa1 = std::chrono::high_resolution_clock::now();
auto aa2 = std::chrono::high_resolution_clock::now();
float aa3 = std::chrono::duration<float>(aa2 - aa1).count();
float xx = fmod(aa3 * -180.f, 360.f); 
auto WeaponManagerComponent = g_LocalPlayer->WeaponManagerComponent;
if (WeaponManagerComponent) {
auto CurrentWeaponReplicated = (ASTExtraShootWeapon *) WeaponManagerComponent->CurrentWeaponReplicated;
if (CurrentWeaponReplicated) {
auto ShootWeaponEntityComp = CurrentWeaponReplicated->ShootWeaponEntityComp;
auto CachedCrossHairComponent = CurrentWeaponReplicated->CachedCrossHairComponent;
if (ShootWeaponEntityComp && CachedCrossHairComponent) {
CachedCrossHairComponent->RotateAngle = xx;
ShootWeaponEntityComp->GameDeviationFactor = 0.0f; 
