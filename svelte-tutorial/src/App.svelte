<script>
  let user = { loggedIn: false };

  function toggle() {
    user.loggedIn = !user.loggedIn;
    console.log("weeee");
    var mark = document.createElement("marquee");
    mark.innerHTML = "Svelte";
    document.body.appendChild(mark);
  }
</script>

{#if user.loggedIn}
  <button on:click={toggle}>Log out</button>
{/if}

{#if !user.loggedIn}
  <button on:click={toggle}>Log in</button>
{/if}
