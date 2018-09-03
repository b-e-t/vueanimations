<template>
<svg xmlns="http://www.w3.org/2000/svg" id="SVGRoot" width="640" height="480">
  <g id="layer1">
    <path id="rect1374" fill="#aef" d="M0 0h640v480H0z"/>
  </g>
  <g id="layer5">
    <g id="g1449" transform="matrix(1.07928 0 0 1.07928 -10.124 69.647)">
      <path id="rect1442" fill="#37483e" d="M245.296 46.704L314.593 153H176z"/>
      <path id="path1445" fill="#536c5d" d="M245.296 46.704L278.593 153H176z"/>
    </g>
    <g id="g1455" transform="matrix(.54538 0 0 .54538 204.301 151.333)">
      <path id="path1451" fill="#37483e" d="M245.296 46.704L314.593 153H176z"/>
      <path id="path1453" fill="#536c5d" d="M245.296 46.704L278.593 153H176z"/>
    </g>
    <g id="g1461" transform="matrix(.78643 0 0 .78643 216.674 114.453)">
      <path id="path1457" fill="#37483e" d="M245.296 46.704L314.593 153H176z"/>
      <path id="path1459" fill="#536c5d" d="M245.296 46.704L278.593 153H176z"/>
    </g>
  </g>
  <g id="layer2">
    <path id="path1398" fill="#006680" stroke-width="1.619" d="M507 236c0 101.068-81.932 183-183 183s-183-81.932-183-183z"/>
  </g>
  <g id="layer3">
    <path id="path1398-9" fill="#00aad4" stroke-width="1.619" d="M507 236c-31 100.068-121.514 118.74-183 71-47.796-37.11-163 29.068-183-71z"/>
  </g>
  <g id="layer4">
    <path id="path1398-9-1" fill="#0cf" stroke-width="1.619" d="M507 236c-58 88.068-101.514 75.74-163 28-47.796-37.11-144 60.068-203-28z"/>
  </g>
  <g id="layer6">
    <path id="rect1464" fill="#71c837" stroke-width=".515" d="M138.755 228.957h370.49v7.086h-370.49z"/>
  </g>
</svg>
</template>

<script>
export default {
  name: 'WorldSpinner'
}
</script>

<style scoped>
  #layer6{/*grass*/
    animation-name: appear;
    animation-duration: 4s;
    animation-delay: 0s;
    animation-iteration-count: infinite;
  }
  #layer5{/*mountains*/
    animation-name: bounce;
    animation-duration: 4s;
    animation-delay: 0s;
    animation-iteration-count: infinite;
  }

  #layer2{/*bottom-back*/
    animation-name: spin;
    animation-duration: 4s;
    animation-delay: 0s;
    animation-iteration-count: infinite;
  }

  #layer3{/*bottom-middle*/
    animation-name: spin;
    animation-duration: 4s;
    animation-delay: 100ms;
    animation-iteration-count: infinite;
  }

  #layer4{/*bottom-top*/
    animation-name: spin;
    animation-duration: 4s;
    animation-delay: 200ms;
    animation-iteration-count: infinite;
  }

  @keyframes appear{
    0%, 10%{
      transform: scale(1);
      transform-origin: 50% 50%;
    }
    10%, 20%{
      transform: scale(0);
      transform-origin: 50% 50%;
    }
    25%, 100%{
      transform: scale(1);
      transform-origin: 50% 50%;
    }
  }

  @keyframes bounce{
    0%{
        transform: translateY(0%);
        transform-origin: 50% 50%;
    }
    4%, 20%{
        transform: translateY(-5%);
    }
    20%{
      transform: scale(0);
    }
    25%{
      transform: translateY(24%);
    }
    32%, 34%{
      transform: scale(1);
      transform: translateY(-5%);
    }
    45%, 100%{
        transform: translateY(0%);
    }
  }

  @keyframes spin{
    0%{
        transform: rotate(0deg);
        transform-origin: 50% 50%;
    }
    3%, 4%{
        transform: rotate(20deg);
        transform-origin: 50% 50%;
    }
    20%, 100%{
        transform: rotate(-360deg);
        transform-origin: 50% 50%;
    }
  }
</style>
