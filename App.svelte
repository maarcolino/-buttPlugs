<script>
  import Login from './components/Login.svelte';
  import Register from './components/Register.svelte';
  
  let showLogin = true;

  const toggleForm = () => {
    showLogin = !showLogin;
  };
</script>

<div>
  <button on:click="{toggleForm}">
    {showLogin ? 'Register' : 'Login'}
  </button>
  {#if showLogin}
    <Login />
  {:else}
    <Register />
  {/if}
</div>
