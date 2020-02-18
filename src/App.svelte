<script>
  import { Router, Link, Route } from "svelte-routing";
  import Red from "./components/red.svelte";
  import Green from "./components/green.svelte";
  import Blue from "./components/blue.svelte";

  export let url = "";
</script>

<Router {url}>
  <nav>
    <Link to="/">Red</Link>
    <Link to="green">Green</Link>
    <Link to="blue">Blue</Link>
  </nav>
  <div>
    <Route path="blue" component={Blue} />
    <Route path="green" component={Green} />
    <Route path="/">
      <Red />
    </Route>
  </div>
</Router>
