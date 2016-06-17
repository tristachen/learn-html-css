# Other

## data attribute
  用來存放小量資訊且對 user 來說不是那麼重要的東西，如果對 user 而言是重要的話，應該要呈現給 user 看，甚至是用 aria attribute。
  不要透過 data-* 去尋找 dom，效能比用 class 要來的差很多。而且定義上來說也不是用來提供 js select 的
