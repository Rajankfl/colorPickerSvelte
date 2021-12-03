<script>
  import "dino-color-picker";

  let color = "#C93B767A";
  let hslaColor = [];
  let rgbaColor = [];
  let hexColor = "";
  const onColorChange = (e) => {
    color = e.target.value;
    hexColor = e.target.value;
    hslaColor = e.target._hsla;
    rgbaColor = e.target._rgba;
  };
</script>

<main style="background-color:{color}">
  <div class="colorsPicker">
    <dino-color-picker on:change={onColorChange} />
    <div class="MoreDetials">
      <!-- Button trigger modal -->
      <button
        type="button"
        class="btn btn-primary ShowMoreButton"
        data-bs-toggle="modal"
        data-bs-target="#exampleModal"
      >
        Show More Details
      </button>

      <!-- Modal -->
      <div
        class="modal fade"
        id="exampleModal"
        tabindex="-1"
        aria-labelledby="exampleModalLabel"
        aria-hidden="true"
      >
        <div class="modal-dialog">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title" id="exampleModalLabel">
                Selected Color Details
              </h5>
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              />
            </div>
            <div class="modal-body" >
				Color Details
			</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</main>

<style>
  main {
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: sans-serif;
    text-align: center;
    flex-direction: column;
    width: 100vw;
    height: 100vh;
  }
  .MoreDetials {
    margin-top: 25px;
  }
  .ShowMoreButton {
    color: white;
    outline: none;
    border: none;
    width: 200px;
    height: 50px;
    border-radius: 50px;
    cursor: pointer;
    background: linear-gradient(
      to right,
      #ff0b847d,
      hsl(180deg 100% 50% / 57%)
    );
  }
</style>
