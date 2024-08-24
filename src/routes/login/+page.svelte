<script>
  let username = '';
  let password = '';
  let email = '';
  let isLoggedIn = false;

  const handleLogin = () => {
    console.log('Login clicked');
    console.log('Username:', username);
    console.log('Password:', password);
    isLoggedIn = true;
  };

  const handleSignup = () => {
    console.log('Sign Up clicked');
    console.log('Username:', username);
    console.log('Password:', password);
    console.log('Email:', email);
    isLoggedIn = true;
  };

  const handleLogout = () => {
    console.log('Logout clicked');
    isLoggedIn = false;
  };
</script>

<style>
 /* CSS style sheet to add to the layout */
body {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  text-align: center;
  font-family: Arial, sans-serif;
}

h1 {
  color: #333;
  margin-bottom: 10px;
}

form {
  width: 100%; /* Adjust the width of the form */
  padding: 20px; /* Add padding to the form */
  box-sizing: border-box;
  border: 1px solid #ddd;
  border-radius: 5px; /* Rounded border */
  transition: border-color 0.3s; /* Smooth transition for border color change */
}

form:hover {
  border-color: #2196f3; /* Border color on hover */
}

table.signup-table {
  width: 100%;
  text-align: left;
  border-collapse: collapse;
  margin-top: 20px;
}

table.signup-table td {
  padding: 8px;
  border-bottom: 1px solid #ddd;
}

input {
  width: calc(100% - 16px); /* Adjust the width to account for padding */
  padding: 8px;
  margin-bottom: 10px;
  box-sizing: border-box;
  border: none; /* Remove individual input borders */
}

button.signup {
  background-color: #2196f3;
  color: white;
  padding: 10px;
  border: none;
  cursor: pointer;
}

button.signup:hover {
  background-color: #0d47a1;
}

</style>

<body>
  {#if isLoggedIn}
    <h1>Welcome, {username}!</h1>
    <button on:click={handleLogout} class="logout">Logout</button>
  {:else}
    <h1>Sign Up Page</h1>
    <form on:submit|preventDefault={handleSignup}>
      <table class="signup-table">
        <tr>
          <td><label for="username">Username:</label></td>
          <td><input type="text" id="username" bind:value={username} /></td>
        </tr>

        <tr>
          <td><label for="password">Password:</label></td>
          <td><input type="password" id="password" bind:value={password} /></td>
        </tr>

        <tr>
          <td><label for="email">Email:</label></td>
          <td><input type="email" id="email" bind:value={email} /></td>
        </tr>

        <tr>
          <td colspan="2"><button type="submit" class="signup">Sign Up</button></td>
        </tr>
      </table>
    </form>
  {/if}
</body>
