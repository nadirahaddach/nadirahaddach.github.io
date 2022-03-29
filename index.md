{% include navigation.html %}

{% include_relative README.md %}

<style>
#video_wrapper {
    margin:0px;
    padding:0px;
}
#video_wrapper video {
    position: fixed;
    top: 50%; left: 50%;
    z-index: -99; important!
    min-width: 100%;
    min-height: 100%;
    width: auto;
    height: auto;
    transform: translate(-50%, -50%);
}
</style>

<div id="video_wrapper">
  <video autoplay loop>
    <source src="https://media3.giphy.com/media/BHNfhgU63qrks/giphy.gif" type="video/mp4">
  </video>
</div>
