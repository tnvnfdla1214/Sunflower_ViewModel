# Sunflower ViewModel
## [StateFlower](https://developer.android.com/kotlin/flow/stateflow-and-sharedflow) & [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel?hl=ko)

먼저 SPA(Single-Page-Application) 구조인 이 프로젝트에서 유일한 액티비티인 GardenActivity의 ViewModel 은 없습니다.

껍데기 역할만 함!

## PlantListViewModel
PlantListFragment의 ViewModel인 PlantListViewModel 입니다.

![image](https://user-images.githubusercontent.com/48902047/149533558-fbc42c36-d79b-445d-ad22-83313769c005.png)

Android Architecture의 Model 에 해당하는 Repository와 SaveStateHandle을 가지고 있습니다.
