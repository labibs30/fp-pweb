<template>
      <div class="container">
        <div class="d-flex align-items-center p-3 my-3 text-white bg-purple rounded shadow-sm" >
            <img class="me-3" src="https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-white.svg" alt="" width="48" height="38">
            <div class="lh-1 container" >
                <div class="top">
                    <h1 class="h6 mb-0 text-white lh-1 bold vertical-center" style="margin-top: 10px;">Amma</h1>
                    <button type="button" class="btn btn-warning text-light bold" data-bs-toggle="modal" data-bs-target="#exampleModal" data-bs-whatever="@mdo">Add Surah</button>
                </div>
            </div>
        </div>
        <!-- /modal/ -->
        <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">
                <div class="modal-header">
                    <h1 class="modal-title fs-5" id="exampleModalLabel">Add Surah</h1>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form>
                    <div class="mb-3">
                        <label for="message-text" class="col-form-label">Surah</label>
                        <div class="input-group mb-3">
                            <span class="input-group-text" id="basic-addon1"><i class="fa-solid fa-magnifying-glass"></i></span>
                            <input type="text" class="form-control" placeholder="search ... " aria-label="Username" aria-describedby="basic-addon1">
                        </div>
                        <div class="form-check form-switch">
                            <input class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckDefault">
                            <label class="form-check-label" for="flexSwitchCheckDefault">An-naba</label>
                        </div>

                    </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary">Send message</button>
                </div>
                </div>
            </div>
        </div>
        <div class="my-3 p-3 bg-body rounded shadow-sm">
            <router-link to="/"><i class="fa-solid fa-arrow-left"></i></router-link>
            <h6 class="border-bottom pb-2 mb-0 bold">All Surah</h6>
              <div >
                <div class="d-flex text-muted pt-3">
                  <strong class="bd-placeholder-img flex-shrink-0 me-3 rounded mt-0.75"   ><text x="50%" y="50%" fill="#007bff" dy=".3em">1</text></strong>

                  
                  <!-- v-for="playlist in playlists" :key="playlist.id" -->
                    <div class="pb-3 mb-0 small lh-sm border-bottom w-100"> 
                        <div class="d-flex justify-content-between">
                          <strong class="text-gray-dark" style="margin-top:7px">MyPl</strong>
                          <audio controls>
                            <source src="http://ia802609.us.archive.org/13/items/quraninindonesia/002AlBaqarah.mp3" type="audio/mpeg">
                          </audio>
                          <div>
                              <router-link class="btn btn-primary" to="/playlist" >Open</router-link>
                              <button class="btn btn-danger" style="margin-left:3px" @click="deletePlaylist(this.id)">Delete</button>
                          </div>
                        <!-- <router-link to="/" class="btn btn-primary">Buka</router-link> -->
                        </div>
                        <!-- <span class="d-block" style="margin-top:-20px">@username</span>  -->
                    </div>
                </div>
              </div>
            <small class="d-block text-end mt-3">
            </small>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
html,
body {
  overflow-x: hidden; /* Prevent scroll on narrow devices */
}

body {
  padding-top: 56px;
}

@media (max-width: 991.98px) {
  .offcanvas-collapse {
    position: fixed;
    top: 56px; /* Height of navbar */
    bottom: 0;
    left: 100%;
    width: 100%;
    padding-right: 1rem;
    padding-left: 1rem;
    overflow-y: auto;
    visibility: hidden;
    background-color: #343a40;
    transition: transform .3s ease-in-out, visibility .3s ease-in-out;
  }
  .offcanvas-collapse.open {
    visibility: visible;
    transform: translateX(-100%);
  }
}

.nav-scroller .nav {
  color: rgba(255, 255, 255, .75);
}

.nav-scroller .nav-link {
  padding-top: .75rem;
  padding-bottom: .75rem;
  font-size: .875rem;
  color: #6c757d;
}

.nav-scroller .nav-link:hover {
  color: #007bff;
}

.nav-scroller .active {
  font-weight: 500;
  color: #343a40;
}

.bg-purple {
  background-color: #42b983;
}
.bd-placeholder-img {
        font-size: 1.125rem;
        text-anchor: middle;
        -webkit-user-select: none;
        -moz-user-select: none;
        user-select: none;
      }

      @media (min-width: 768px) {
        .bd-placeholder-img-lg {
          font-size: 3.5rem;
        }
      }

      .b-example-divider {
        height: 3rem;
        background-color: rgba(0, 0, 0, .1);
        border: solid rgba(0, 0, 0, .15);
        border-width: 1px 0;
        box-shadow: inset 0 .5em 1.5em rgba(0, 0, 0, .1), inset 0 .125em .5em rgba(0, 0, 0, .15);
      }

      .b-example-vr {
        flex-shrink: 0;
        width: 1.5rem;
        height: 100vh;
      }

      .bi {
        vertical-align: -.125em;
        fill: currentColor;
      }

      .nav-scroller {
        position: relative;
        z-index: 2;
        height: 2.75rem;
        overflow-y: hidden;
      }

      .nav-scroller .nav {
        display: flex;
        flex-wrap: nowrap;
        padding-bottom: 1rem;
        margin-top: -1px;
        overflow-x: auto;
        text-align: center;
        white-space: nowrap;
        -webkit-overflow-scrolling: touch;
      }

.bold{
    font-weight: bold;
    text-align: center;

    /* vertical-align: middle; */
}
.top{
    display: flex;
    justify-content: space-between;
}
</style>