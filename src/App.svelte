<script>
  let numbers = [1,2,3,4];

  function addNumber() {
    // numbers.push(numbers.length + 1);
    // numbers = numbers;
    numbers = [...numbers, numbers.length + 1];
  }

  $: sum = numbers.reduce((t, n) => t + n, 0);

  // function incrementCount() {
  //   count += 1;
  // }
</script>

<p>{numbers.join(" + ")} = {sum}</p>

<button on:click={addNumber}>Add a number</button>

<!-- <button on:click={incrementCount}>
  Clicked {count} {count === 1 ? "time" : "times"}
</button>

<p>{count} doubled is {doubled}</p> -->
