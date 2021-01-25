<style lang="scss">
  .stories {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    margin: 1em 0;
    padding: 0.5em 1em;
    background-color: white;

    .container {
      .head {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0.5em 0 0 0;
        h2 {
          font-size: 12px;
          font-weight: 600;
        }
        span {
          font-size: 12px;
          font-weight: normal;
          color: black;
          cursor: pointer;
        }
      }

      .items {
        margin: 0.5em 0 0.5em 0;

        .item {
          display: flex;
          align-items: center;
          margin: 0 0 0.5em 0;

          img {
            width: 32px;
            height: 32px;
            border-radius: 50%;
          }

          h2 {
            font-size: 14px;
            color: black;
            margin: 0 0 0 0.5em;
            span {
              display: block;
              font-size: 9px;
              text-transform: uppercase;
              color: gray;
            }
          }

          .item-box {
            width: 32px;
            height: 32px;
            border: double 2px transparent;
            border-radius: 100%;
            background-image: linear-gradient(#fff, #fff),
              radial-gradient(circle at top left, #f09433, #bc1888);
            background-origin: border-box;
            background-clip: content-box, border-box;
          }
        }
      }
    }
  }
</style>

<div class="stories">
  <div class="container">
    <div class="head">
      <h2>Historias</h2>
      <span>Ver todas</span>
    </div>
    <div class="items">
      {#each Array(3) as _, i}
        <div class="item">
          <div class="item-box">
            <img
              src={`https://arepa.s3.amazonaws.com/elmo00${i + 2}.jpg`}
              alt="profile"
            />
          </div>
          <h2> 
            nickname{i === 0 ? 1 : i + 1}
            <span>{`${Math.floor(Math.random() * (10 - i + i)) + i} horas antes`}</span>
          </h2>
        </div>
      {/each}
    </div>
  </div>
</div>
