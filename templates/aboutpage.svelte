<script>
  const endpoint = "http://localhost:8080/users";
  async function getall(){
    let response = await fetch(endpoint, {mode:'cors'})
    data = await response.json()
    console.log(data)
    let el = document.getElementById("people")

    data.forEach(element => {
      el.textContent += element.username 
    });
  }
  getall()
  var data
</script>

<main>
  <h1>Hello Gay!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
  <p id="people"></p>
</main>

<style>
  /* ommitted for brevity */
</style>
