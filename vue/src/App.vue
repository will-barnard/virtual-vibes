<template>

  <div class="appDisplay" >
    <NavComp class="navDisplay" v-bind:key="$store.state.token"/>
    <div class="main-body">
      <SiteHeader />
      <div class="routing">
        <router-view v-bind:key="$route.fullPath" />
      </div>
    </div>
    
  </div>

</template>


<script>
import NavComp from './components/NavComp.vue'
import SiteHeader from './components/SiteHeader.vue'

export default {
  components: {NavComp, SiteHeader}
}
</script>

<style>
:root {
  --background-color: #fdf6e3; /* Soft cream */
  --main-text-color: #2e2e2e; /* Deep charcoal */
  --header-bg-color: #8c7ae6; /* Vibrant lavender */
  --hover-color: #f39c12; /* Bright orange for hover effects */
  --nav-bg-color: #6c5ce7; /* Rich purple for navigation */
  --post-bg-color: #ffeaa7; /* Warm pastel yellow for posts */
  --downvote-color: #e74c3c; /* Bright red for downvotes */
  --gold-color: #f1c40f; /* Vibrant gold */
  --white-color: #ffffff; /* White */
  --black-color: #000000; /* Black */
  --light-gray: #dfe6e9; /* Soft gray for hover effects */
}

/* general */
body {
  font-family: Avenir;
  overflow: hidden;
  margin: 0px;
  background-color: var(--background-color);
}
.main-body {
  overflow-y: scroll;
  flex-grow: 1;
  color: var(--main-text-color);
}
.site-header {
  background-color: var(--header-bg-color);
  color: var(--main-text-color);
}
.site-header h1:hover {
  color: var(--hover-color);
}
/* nav */
.nav-closed,
.nav-open {
  background-color: var(--nav-bg-color);
  color: var(--main-text-color);
}
.nav h3:hover,
.nav h4:hover {
  color: var(--hover-color);
}
nav img {
  background-color: var(--main-text-color);
}
nav img:hover {
  background-color: var(--hover-color);
}
.box {
  background-color: var(--white-color);
}
.box:hover {
  background-color: var(--light-gray);
}
/* forums view */
.forum {
  background-color: var(--header-bg-color);
}
.forum:hover {
  background-color: var(--hover-color);
}
/* post view */
.post {
  background-color: var(--post-bg-color);
}
.downvoted {
  color: var(--downvote-color);
}
.unfavorite {
  background-color: var(--gold-color);
}
.reply {
  background-color: var(--white-color);
}
.reply:hover {
  background-color: var(--light-gray);
}
/* comments */
.comments {
  background-color: var(--post-bg-color);
}
.comment {
  background-color: var(--white-color);
}
.commentsBox {
  background-color: var(--hover-color);
}
.backToForum {
  background-color: var(--nav-bg-color);
  color: var(--main-text-color);
}
.backToForum:hover {
  background-color: var(--main-text-color);
  color: var(--black-color);
}
/* login */
.logBox {
  background-color: var(--white-color);
}
.logBox h2:hover {
  background-color: var(--header-bg-color);
  color: var (--white-color);
}

/*  */
/* general */
/*  */

@font-face {
    font-family: Avenir;
    src: url(src/assets/fonts/Avenir-Regular.ttf);
}
@font-face {
    font-family: Sen;
    src: url(src/assets/fonts/Sen-Regular.ttf);
}


body{
  font-family: Avenir;
    overflow: hidden;
    margin: 0px;
    background-color: var(--background-color);
}
.main-body {
    overflow-y: scroll;
    flex-grow: 1;
    color: var(--main-text-color);
}
.routing{
    margin-left: 10px;
}
.appDisplay{
  display: flex;
  flex-direction: row;
  width: 100vw;
  height: 100vh;
  margin-bottom: 10px;
}
section {
    flex: 1 1 auto;
    overflow: auto;
}
p {
    padding: 0px;
    margin: 1px;
}
.site-header {
    background-color: var(--header-bg-color);
    margin: 0px;
    color: var(--main-text-color);
}
.site-header h1 {
    display: inline-block;
    cursor: pointer;
    margin: 0px;
    padding: 15px;
    transition: .5s;
}
.site-header h1:hover {
    color: var(--hover-color);
    transition: .5s;
}
/*  */
/* nav */
/*  */

.nav-closed {
    background-color: var(--nav-bg-color);
    border: 2px;
    color: var(--main-text-color);
    padding-top: 3px;
    padding-bottom: 3px;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: start;
    width: 47px;
    transition: all .6s ease;
}
.nav-open {
    background-color: var(--nav-bg-color);
    border: 2px;
    color: var(--main-text-color);
    padding-top: 3px;
    padding-bottom: 3px;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: start;
    width: 150px;
    transition: all .5s ease;
}
.nav{
    display: flex;
    flex-direction: column;
    padding: 5px;
    width: 150px;
}
.nav h3 {
    padding-left: 10px;
    margin: 4px;
    text-decoration: underline;
    cursor: pointer;
}
.nav h3:hover{
    color: var(--hover-color);
}
.nav h4 {
    padding-left: 10px;
    margin: 4px;
    text-decoration: underline;
    cursor: pointer;
    font-weight: 300;
    transition: .2s;
}
.nav h4:hover{
    color: var(--hover-color);
    transition: .2s;
}
#navHeader {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: start;
}
nav img {
    width: 50px;
    border: 2px black solid;
    border-radius: 50px;
    align-self: center;
    margin-right: 10px;
    background-color: var(--main-text-color);
    cursor: pointer;
    transition: .2s;
}
nav img:hover {
    transform:scale(1.3);
    background-color: var(--hover-color);
    transition: .5s;
}
#favorites {
    margin-bottom: 10px;
}
#favorites:hover{
    cursor: default;
    color: var(--main-text-color);
}
.title{
    border: 2px;
    border-radius: 5px;
    padding: 4px;
    cursor: pointer;
    text-decoration: underline;
}
#hello-msg {
    text-decoration: none;
    cursor: default;
    align-self: center;
    margin-right: 10px;
}
#hello-msg:hover {
    color: var (--main-text-color);
}
#nav-spacer {
    flex-grow: 1;
}
.nav-container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex-grow: 1;
}
.nav-footer {
    margin-bottom: 15px;
    display: flex;
    flex-direction: column;
    padding: 5px;
    width: 150px;
}
/*  */
/* containers */
/*  */

.container {
  display: inline-block;
  cursor: pointer;
  padding: 5px;
}

.wrapped {
    border: 2px black solid;
    border-radius: 10px;
    background-color: var(--hover-color);
}

.box {
    border: 2px black solid;
    margin: 5px;
    padding: 3px;
    border-radius: 8px;
    cursor: pointer;
    background-color: var(--white-color);
}
.box:hover {
    background-color: var(--light-gray);
    transition: 0.1s;
}

/*  */
/* forums view */
/*  */

.forum {
    border: 2px solid black;
    border-radius: 10px;
    background-color: var(--header-bg-color);
    cursor: pointer;
    padding: 5px;
    margin: 3px;
    width: 50vw;
    transition: .3s;
}
.forum:hover {
    background-color: var(--hover-color);
    transition: 0.3s;
}
.list h2 {
    margin: 1px;
}
.list p {
    margin: 1px;
}
.header-forum {
    display: flex;
    justify-content: space-between;
    margin: 10px;
    margin-bottom: 20px;
    width: 50vw;
    align-items: flex-end;
}
.header-forum form {
    margin-top: 15px;
    margin-bottom: 15px;
}
.header-forum h3{
    cursor: pointer;
    border: 2px black solid;
    border-radius: 5px;
    display: inline;
}
.header-forum h1 {
    text-decoration: underline;
    display: inline;
}
.header-forum h3 {
    display: inline;
    border-radius: 20px;
    padding: 5px;
}
.header-forum div {
    display: inline;
}
.favorite {
    font-size: 1.2em;
    background-color: var(--white-color);
    color: var (--header-bg-color);
    transition: .5s;
}
.unfavorite {
    font-size: 1.2em;
    background-color: var(--gold-color);
    color: var (--header-bg-color);
}
.create-forum {
    display: flex;
    color: var(--main-text-color);
    justify-content: flex-end;
    width: 50vw;
}
.create-forum h3 {
    display: inline-block;
    border: 2px solid black;
    border-radius: 10px;
    padding: 5px;
    background-color: var(--header-bg-color);
    transition: 0.2s;
    margin-left: 5px;
    cursor: pointer;
}
.create-forum h3:hover {
    background-color: var(--white-color);
    color: var(--black-color);
}

/*  */
/* forum view */
/*  */

.active-button {
    background-color: var(--hover-color);
}

.form-input-group {
  margin-bottom: 1rem;
}
label {
  margin-right: 0.5rem;
}
.post-list {
    background-color: var(--header-bg-color);
    width: 50vw;
    transition: .3s;
}
.post-list h2 {
    margin: 1px;
}
.post-list p {
    margin: 1px;
}
.post-list:hover{
    background-color: var(--hover-color);
    transition: .3s;
}

/*  */
/* post view */
/*  */

.postHeader h1 {
    margin-bottom: 1px;
}

.subHeader {
    display: flex;
    flex-direction: row;
    align-items: center;
}
.subHeader p {
    margin-top: 5px
}
.postBody {
    border: 2px solid black;
    border-radius: 10px;
    padding: 10px;
    margin: 10px;
    background-color: var(--nav-bg-color);
}
.postContent {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.postHeader {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.post {
    border: 2px black solid;
    border-radius: 10px;
    padding: 15px;
    margin: 2px;
    background-color: var(--post-bg-color);
    flex-grow: 1;
}
.upvoted {
    color: var(--hover-color);
}
.downvoted {
    color: var(--downvote-color);
}
.url-image {
    border: 2px;
    border-radius: 15px;
    width: 30vw;
}
.deletePost {
    font-size: 2em;
    cursor: pointer;
}
.voteCount {
    display: inline-block;
    margin-right: 10px;
}
.enableVote {
    cursor: pointer;
}
.disableVote {
    cursor: default;
}
#cancelButton {
  color: var(--black-color);
  text-decoration: none;
}
.postForm {
    margin-top: 15px;
    margin-bottom: 15px;
}
.postForm textarea {
    width: 40vw;
    height: 5vh;
    resize: none;
    border: 2px solid;
    border-radius: 5px;
}
/*  */
/* comments */
/*  */
.comment {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
.deleteComment {
    font-size: 1.5em;
    cursor: pointer;
}
.comments{
    border: 2px black solid;
    border-radius: 10px;
    background-color: var(--post-bg-color);
    padding: 5px;
    margin-top: 5px;
    margin-bottom: 5px;
    color: var(--header-bg-color);
}
.comment{
    border: 2px black solid;   
    border-radius: 10px;
    padding: 3px;
    margin: 2px;
    background-color: var(--white-color);
}
.noComments{
    font-style: italic;
}
.commentsBox{
    border: 2px solid black;
    border-radius: 10px;
    background-color: var(--hover-color);
    padding: 5px;
    margin-right: 10px;
}
.backToForum {
    display: inline-block;
    border: 2px solid black;
    border-radius: 5px;
    padding: 5px;
    background-color: var(--nav-bg-color);
    color: var(--main-text-color);
    cursor: pointer;
    transition: 0.2s;
}
.backToForum:hover{
    background-color: var(--main-text-color);
    color: var(--black-color);
}
.reply {
    font-size: .75em;
    cursor: pointer;
    margin: 1px;
    padding: 3px;
    border: 1px black solid;
    border-radius: 5px;
    display: inline-block;
    background-color: var(--white-color);
    transition: 0.2s;
    color: var(--header-bg-color);
}
.reply-box textarea {
    width: 40vw;
    height: 5vh;
    resize: none;
    border: 2px solid;
    border-radius: 5px;
}
.reply:hover {
    background-color: var(--light-gray);
}
.replyPost {
    font-size: 1em;
    cursor: pointer;
    margin-top: 15px;
    margin-bottom: 15px;
    padding: 5px;
    border: 1px black solid;
    border-radius: 5px;
    display: inline-block;
    background-color: var(--white-color);
    transition: 0.2s;
    color: var(--header-bg-color);
}
.replyPost:hover {
    background-color: var(--light-gray);
}
#authorName {
    margin-top: 0;
    margin-right: 4px;
    text-decoration: underline;
    font-size: 1.5em;
    color: var(--main-text-color);
    cursor: pointer;
}
/*  */
/* new post */
/*  */
.new-post-form{
    width: 25vw;
    border: 2px var(--header-bg-color) solid;
    border-radius: 10px;
    margin-top: 20px;
    padding: 15px;
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
    
}
.new-post-form h1 {
    text-align: center;
}
.new-post-form form {
    text-align: left;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    gap: 5px;
}
.new-post-sub {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-content: center;
    gap: 5px;
}
.new-post-sub input {
    flex-grow: 1;
}
.new-post-form textarea {
    margin-bottom: 5px;
    resize: none;
    width: 25vw;
}
/*  */
/* login */
/*  */
.logBox-container {
    display: inline-block;
    padding: 15px;
}
.logBox{
    color: var(--header-bg-color);
  border: 2px solid black;
  border-radius: 10px;
  background-color: var(--white-color);
  padding: 15px;
  padding-bottom: 25px;
  margin: 20px;
  text-align: center;
}
.logBox h2{
  display: inline;
  padding: 5px;
  border: 2px black solid;
  border-radius: 5px;
  background-color: var(--white-color);
  cursor: pointer;
}
.logBox h2:hover{
  background-color: var(--header-bg-color);
  color: var(--white-color);
  transition: .3s;
}
.form-input-group {
  margin-bottom: 1rem;
}
label {
  margin-right: 0.5rem;
}

/*  */
/* loading */
/*  */

.show-div {
    transition: opacity .8s ease .2s;
    opacity: 100%;
}
.hide-div{
    transition: opacity .8s ease .2s;
    opacity: 0%;
}

/*  */
/* animations */
/*  */

.bar1, .bar2, .bar3 {
    width: 35px;
    height: 5px;
    background-color: var(--main-text-color);
    margin: 6px 0;
    transition: 0.4s;
  }
  .fade-enter-active{
      transition: opacity .8s ease .2s;
  }
  .fade-leave-active {
    transition: opacity .15s ease;
  }
  
  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }

  .fadeComment-enter-active{
    transition: opacity .6s ease;
}
.fadeComment-leave-active {
}

.fadeComment-enter-from,
.fadeComment-leave-to {
  opacity: 0;
}
  
  /* Rotate first bar */
  .change .bar1 {
    transform: translate(0, 11px) rotate(-90deg);
  }
  /* Fade out the second bar */
  .change .bar2 {
      opacity: 0;
      transition: 0.1s;
  }
  /* Rotate last bar */
  .change .bar3 {
    transform: translate(0, -11px) rotate(90deg);
  }
</style>

