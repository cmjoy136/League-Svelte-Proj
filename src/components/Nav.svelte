  
  <style>
      .nav-container{
          display: flex;
          justify-content: flex-start;
          align-items: center;
      }
    .nav-bar {
      list-style-type: none;
      display: flex;
      justify-content: space-evenly;
      width: 25%;
      height: 40px;
      margin: 0;
      padding: 0;
    }
    .nav-bar li{
        display: flex;
        width: 75px;
        justify-content: center;
        align-items: center;
        background-color: yellow;
        border-radius: 5px;
    }
    .nav-bar li:hover{
        background-color: lightgoldenrodyellow;
        border: 1px solid yellow;

    }
  </style>
<div class="nav-container">
  <ul class="nav-bar">
    <li>Home</li>
    <li>Login</li>
    <li>Profile</li>
  </ul>
</div>
