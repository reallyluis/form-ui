<!-- App.svelte -->
<script>
  let questions = [];
  let question = '';

  const addQuestion = () => {
    questions = [
      ...questions,
      question,
    ];

    question = '';
  };
</script>
<style>
  /* css will go here */
</style>
<div class="App">
  <header class="App-header">
    FORM
    <ul>
      {#each questions as quest}
      <li>{quest}</li>
      {/each}
    </ul>
    <div>
      <input type="text" name="question" bind:value={question} />
      <button type="button" on:click={addQuestion}>Add</button>
    </div>
  </header>
</div>