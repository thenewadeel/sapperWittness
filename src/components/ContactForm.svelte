<script>
  import Form from '@svelteschool/svelte-forms';
  let values;
</script>

<style>
  /* label {
          display: inline;
      }
      ul {
          list-style: none;
          display: flex;
          padding: 0;
      }
      li {
          padding: 0 10px;
      }
      fieldset {
          padding: 10px 0;
          border: none;
      } */
</style>

<Form bind:values>
  <fieldset>
    <input placeholder="First name" type="text" name="firstName" />
    <input placeholder="Last name" type="text" name="lastName" />
  </fieldset>
  <fieldset>
    <input placeholder="Enter email" type="email" name="email" />
    <input placeholder="Phone Number" type="numeric" name="phone" />
  </fieldset>
  <div class="input">
    <label>How did you find us?</label>
    <ul>
      <li>
        <input id="m1" type="checkbox" name="referal" value="Social Media" />
        <label for="m1">Social Media</label>
      </li>
      <li>
        <input id="m2" type="checkbox" name="referal" value="TV" />
        <label for="m2">TV</label>
      </li>
      <li>
        <input id="m3" type="checkbox" name="referal" value="A Friend" />
        <label for="m3">A Friend</label>
      </li>
      <li>
        <input id="m4" type="checkbox" name="referal" value="Search Engine" />
        <label for="m4">Search Engine</label>
      </li>
    </ul>
  </div>

  <label for="interest">Select Interests:</label>
  <select id="interest" name="interest">
    <option value="ERP">ERP Software</option>
    <option value="Business">Business Solution</option>
    <option value="App">Desktop / Mobile App</option>
  </select>
</Form>
<button>Save Info</button>
<!-- <pre>{JSON.stringify(values, undefined, 1)}</pre> -->

<!-- <button on:click={() => values = { ...values, firstName: "WOW! Two-way bound! Amazing!" }}>
      Check 'dat two-way binding!
  </button> -->

