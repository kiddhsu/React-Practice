


`修復新 webpack 版本的 webpack 錯誤`

###### npm run build引發錯誤：error: unknown option '-p'

###### **解法:**
###### package.json內的webpack -p
###### 更改為 --mode production


`修復新 npm run start 無法執行`
###### **解法:**
###### devServer: { 
######     // contentBase: './dist',
######     static: './dist',
######   },


`inline style`

###### 1. 用駝峰式取得 CSS 樣式名稱，且不能有 - 號<br>
###### 若要使用 CSS 的短橫線，可將所有的 key 都變成字串<br>
###### 2. Component 的字首須為大寫字母


`生命週期`
###### 1. Component Render 完畢。
###### 2. Component 內的 State 改變。
###### 3. Component 被移除時。


`Prop-Types`
###### 1. 父層 Component 將某些資料或事件交給子層 Component<br>
###### 2. prop type 錯誤時，是否傳入不正確的 Props 型別


`Redux 資料管理`
###### 1. 資料放到 Store 中儲存，並以 useSelector 將資料取出<br>
###### 2. 將資料層抽離在Redux 中， Component只需向 Redux 取資料，然後負責畫面的呈現


`Redux 事件處理`
###### 1. Reducer會根據 action.type 來判斷要做什麼事情<br>
###### 2. Redux 流程為先對 Component 做 connect，之後便可使用 Store 的 dispatch 觸發預先在 Reducer 中寫好的邏輯


`設置  Middleware`
###### 1. Redux 中用上了不只一個 Middleware，redux-logger一定要設置在最後一個<br>
###### 2. Middleware 會在 Store 和 Reducer 之間，所有透過 Dispatch 的執行都會經過 Middleware


`設置  Redux Saga (請求 API)`
######  Redux-Saga 的流程同樣是先對 Component 做 connect，<br>
######  但 dispatch 觸發的事件為 React-Saga 預先訂閱的名稱，<br> 
######  在該事件裡才依照流程去觸發需執行的 Reducer 邏輯


`SPA(單頁應用程式)`
###### 針對 Url 的變化，來決定顯示哪個 Component 作為當前頁面
