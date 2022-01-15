# Sunflower ViewModel
## [StateFlower](https://developer.android.com/kotlin/flow/stateflow-and-sharedflow) & [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel?hl=ko)

먼저 SPA(Single-Page-Application) 구조인 이 프로젝트에서 유일한 액티비티인 GardenActivity의 ViewModel 은 없습니다.

껍데기 역할만 함!

## PlantListViewModel
PlantListFragment의 ViewModel인 PlantListViewModel 입니다.

![image](https://user-images.githubusercontent.com/48902047/149533558-fbc42c36-d79b-445d-ad22-83313769c005.png)

Android Architecture의 Model 에 해당하는 Repository와 SaveStateHandle을 가지고 있습니다.

ViewModel의 데이터나 함수들은 코루틴과 연관이 많이 되어있습니다.

데이터는 MutableStateFlow 를 사용하는데 상태를 업데이트하고 Flow에 전송하는 것입니다.

그리고 viewModelScope 라는게 보이는데 개념은 다음과 같습니다.

ViewModelScope는 앱의 각 ViewModel을 대상으로 정의됩니다. 이 범위에서 시작된 모든 코루틴은 ViewModel이 삭제되면 자동으로 취소됩니다. 코루틴은 ViewModel이 활성 상태인 경우에만 실행해야 할 작업이 있을 때 유용합니다. 예를 들어 레이아웃의 일부 데이터를 계산한다면 작업의 범위를 ViewModel로 지정하여 ViewModel을 삭제하면 리소스를 소모하지 않도록 작업이 자동으로 취소됩니다. 

## PlantDetailViewModel

PlantDetailFragment의 ViewModel인 PlantDetailViewModel 입니다.

![image](https://user-images.githubusercontent.com/48902047/149606593-f1f71948-e76c-4fcf-b33e-2191b9339d52.png)

Repository로부터 데이터를 불러오고 Flow의 확장함수인 asLiveData()를 사용하여 Flow -> LiveData로 변환시켜줍니다.

## GardenPlantingListViewModel

GardenFragment의 ViewModel인 GardenPlantingListViewModel 입니다.

