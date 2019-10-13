<template>
  <div class="contact">
    <div class="top container bg-light">
      Contact Me.
    </div>
    <div class="bottom">
      <div class="mt-5 h4">
        You can contact me from below!
      </div>
      <hr class="mb-5 mt-0 d-inline-block mx-auto" style="width: 27em;">
      <div class="container bg-light py-5">
        <table class="table table-bordered">
          <thead>
            <tr>
              <th scope="col">#</th>
              <th scope="col">SERVICE</th>
              <th scope="col">@ME</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">1</th>
              <td>
                <font-awesome-icon :icon="['fas','envelope-square']" class="text-dark"/>
                EMAIL
              </td>
              <td>
                <a href="mailto:shunyaendoh.1215@gmail.com">
                  shunyaEndoh.1215@gmail.com
                </a>
              </td>
            </tr>
            <tr>
              <th scope="row">2</th>
              <td>
                <font-awesome-icon :icon="['fab','twitter']" class="text-dark"/> 
                TWITTER
              </td>
              <td>
                <a href="https://twitter.com/shunya39836817">
                  @shunya39836817
                </a>
              </td>
            </tr>
            <tr>
              <th scope="row">3</th>
              <td>
                <font-awesome-icon :icon="['fab','instagram']" class="text-dark"/>                 
                INSTAGRAM
              </td>
              <td>
                <a href="https://www.instagram.com/se_1215/?hl=ja">
                  @se_1215
                </a>
              </td>
            </tr>
            <tr>
              <th scope="row">4</th>
              <td>
                <font-awesome-icon :icon="['fab','facebook']" class="text-dark"/>                                
                FACEBOOK
              </td>
              <td>
                <a href="https://www.facebook.com/endoh.shunya.5">
                  Endoh Shunya
                </a>
              </td>
            </tr>
            <tr>
              <th scope="row">5</th>
              <td>
                <font-awesome-icon :icon="['fab','github']" class="text-dark"/>                                                
                GITHUB
              </td>
              <td>
                <a href="https://github.com/shunyaendoh1215">
                  shunyaendoh1215
                </a>
              </td>
            </tr>
            <tr>
              <th scope="row">6</th>
              <td>
                <font-awesome-layers>
                  <font-awesome-icon :icon="['fas','square']" class="text-dark"/>
                  <font-awesome-icon :icon="['fas','search']" transform="shrink-1" :style="{ color: 'white' }" />
                </font-awesome-layers>              
                QIITA
              </td>
              <td>
                <a href="https://qiita.com/shunyaendoh">
                  shunyaendoh
                </a>
              </td>
            </tr>
          </tbody>
        </table>

        


      </div>

      
    </div>
  </div>
</template>
<style>
.contact {
    padding-bottom: 6rem;
}
</style>
