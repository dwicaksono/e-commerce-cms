<template>
  <div class="bigContainer">
    <nav class="boxNav">
      <div class="navBoxContent">
        <h3>WearIsysm</h3>
      </div>
      <div class="navBoxContent" style="width:25em">
        <div class="wrapper">
          <div class="searchBar">
            <input
              id="searchQueryInput"
              type="text"
              name="searchQueryInput"
              placeholder="Search"
              value
            />
            <button id="searchQuerySubmit" type="submit" name="searchQuerySubmit">
              <svg style="width:24px;height:24px" viewBox="0 0 24 24">
                <path
                  fill="#666666"
                  d="M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
      <div class="navBoxContent">
        <div id="shoppingBag" class="iconNavbar">
          <img src="../assets/shopping-bag.svg" alt />
        </div>
        <div id="loginUser">
          <img src="../assets/log-in.svg" alt />
        </div>
      </div>
    </nav>
    <div class="loginregisBox">
      <LoginPage />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import LoginPage from "../components/Login";
export default {
  name: "Home",
  components: {
    LoginPage
  }
};
</script>
<style  scoped>
.bigContainer {
  background-color: #fff;
  padding: 1em 2em;
  border-radius: 2em;
  height: 75vh;
}
.boxNav {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  justify-items: center;
  text-align: center;
}
.navBoxContent {
  justify-content: center;
  /* width: 100%; */
  /* padding: 0px 2em; */
  display: flex;
  justify-items: center;
  align-items: center;
  flex-wrap: wrap;
}
.navBoxContent h3 {
  letter-spacing: 2px;
}
.iconNavbar {
  margin: 2px 1em;
}
#loginUser,
#shoppingBag {
  cursor: pointer;
}
.loginregisBox {
  display: flex;
  align-items: center;
  justify-content: center;
  justify-items: center;
  padding: 5em 0px;
}
.boxline {
  border: 1px solid black;
}
body {
  font-family: "Roboto", Arial, sans-serif;
}

.wrapper {
  width: 100%;
  max-width: 35rem;
  margin: 0 auto;
}

.label {
  font-size: 0.625rem;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: +1.3px;
  margin-bottom: 1rem;
}

.searchBar {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
}

#searchQueryInput {
  width: 100%;
  height: 2.8rem;
  background: #f5f5f5;
  outline: none;
  border: none;
  border-radius: 0.6rem;
  padding: 0 3.5rem 0 1.5rem;
  font-size: 1rem;
}

#searchQuerySubmit {
  width: 3.5rem;
  height: 2.8rem;
  margin-left: -3.5rem;
  background: none;
  border: none;
  outline: none;
}

#searchQuerySubmit:hover {
  cursor: pointer;
}
</style>
