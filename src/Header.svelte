<script>
  import { username, user } from './user';

  function signout() {
    user.leave();
    username.set('');
  }
</script>

<header>
<h1>😔👍</h1>
  {#if $username}
    <div class="user-bio">
      
      <span>Yo <strong>{$username}</strong></span>
      <img src={`https://avatars.dicebear.com/api/adventurer/${$username}.svg`} alt="avatar" /> 
    </div>

    <button class="signout-button" on:click={signout}>Sign Out</button>

    {:else}

      <h3>you are not ready</h3>
  {/if}
</header>