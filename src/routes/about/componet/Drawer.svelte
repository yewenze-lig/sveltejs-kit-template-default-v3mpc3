<script>
  import { Drawer, Button, CloseButton } from 'flowbite-svelte'
  import { sineIn } from 'svelte/easing';
 import  Nav from './Nav.svelte';
import  FixedSideBar from './FixedSideBar.svelte';
  let hidden9 = true;
  let transitionParams = {
    x: -320,
    duration: 200,
    easing: sineIn
  };
</script>

<div class="text-center">
  <Button on:click={() => (hidden9 = false)}>Show drawer</Button>
</div>

<Drawer
  leftOffset="top-0 h-screen left-0"
  transitionType="fly"
  {transitionParams}
  bind:hidden={hidden9}
  id="sidebar9">

<FixedSideBar/>
</Drawer>