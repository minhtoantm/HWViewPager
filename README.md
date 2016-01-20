



# HWViewPager

- Inherited "UICollectionView"
- looks likes Android's ViewPager
- Preview Left Right Side Partially


## Supported
- **Full Screen in "Auto Layout"**
- **or Preview Left Right Side partially**
- **Auto Fit - Orientation Rotate**
- **Page Selected Delegate Protocol Supported**



## Requirements

- **UICollectionViewFlowLayout**
- **Don't Use SectionView in UICollectionView**
- **Initialize by Storyboard or [initwithFrame: collectionViewLayout:(UICollectionViewFlowLayout*) flowLayout]**


## CocoaPods
```
platform :ios, '8.0'
pod 'HWViewPager'
```

## Programming in Swift?
#### Visit [HWSwiftyViewPager](https://github.com/vowed21/HWSwiftyViewPager)




## Usage

#### Full Screen in "Auto Layout"
- Configure "Section Inset" Left = 0, Right = 0, minimumLineSpacing = 0 ... in FlowLayout (Use storyboard) 
- or :: [collectionViewFlowLayout setSectionInset:UIEdgeInsetsMake(0, 0, 0, 0)]; [collectionViewFlowLayout setMinimumLineSpacing:0];


#### Preview Side (Left, Right) partially"
- Configure "SectionInset" Value Left, Right. And minimumLineSpacing


#### Set Currnet Page
```
-(void) setPage:(NSInteger)page isAnimation:(BOOL)isAnim;
```

##Protocol

HWViewPagerDelegate

```
-(void)pagerDidSelectedPage:(NSInteger)selectedPage
```

- `Connect 'pagerDelegate' IBOutlet  by Storyboard`
- `or [HWViewPager setPagerDelegate:id<HWViewPagerDelegate];`



## License

`HWViewPager` is available under the MIT license. See the LICENSE file for more info.



#Example

## Part of Side Preview || Full

<p align="center" >
  <img src="https://scontent-b.xx.fbcdn.net/hphotos-xfp1/t31.0-8/10922361_828736803853340_8377129052548269031_o.jpg">
</p>



##Auto Fit - Orientation Rotate

<p align="center" >
  <img src="https://scontent-a-sea.xx.fbcdn.net/hphotos-xpa1/v/t1.0-9/10931157_828591637201190_6402771892877942380_n.jpg?oh=198c8ccf58f865b38d00cb854ef339eb&oe=5527A4CD">
</p>



# HWViewPager

- 양 옆이 짤리는 페이저 찾다가, 어떤 뷰든지 범용으로 쓰고 싶어서, 한번 직접 만들어봤습니다.
- 더 좋은 아이디어가 있으신 분들은 코멘트 많이 부탁드립니다.
- UICollectionView 를 상속받아서 만들었습니다.
- 별것 아닌 허잡한 코드지만, 깃허브에 꼭 한번 올려보고 싶었어요. 코멘트 주시면 감사히 받겠습니다.



## 사용

- 스토리보드를 사용하는게 정신건강에 좋습니다.

#### 풀스크린
- 스토리보드에서 "CollectionView"에 있는 SectionInset 의 여백들과 minimumLineSpacing 을 모두 0으로 주시면 그냥 풀로 보입니다.

#### 양 옆이 조금씩 짤려 보이는 페이저.

- SectionInset 의 값들과 minimumLineSpacing 을 적당히 주시면 저절로 양옆이 보이기 시작합니다.


##Protocol

HWViewPagerDelegate

```
-(void)pagerDidSelectedPage:(NSInteger)selectedPage
```

- 델리게이트를 설정해 놓으면, 페이지가 선택될 때마다 이 메소드를 호출할겁니다.
- 스토리보드에 "pagerDelegate" 라는 이름으로 Outlet 만들어놨으니, 그냥 연결해서 쓰셔도 되고,
- 코드로 설정하려면 `[HWViewPager setPagerDelegate:id<HWViewPagerDelegate];` 쓰시면 됩니다.



## License

`HWViewPager` is available under the MIT license. See the LICENSE file for more info.

- 라이센스까지 붙일 코드같진 않지만...







