
# Title

## html

```sh
          <div class="active-calories">
            <h1 style="align-self: flex-start">Active Calories</h1>
            <div class="active-calories-container">
              <div class="box" style="--i: 95%">
                <div class="circle">
                  <h2>85<small>%</small></h2>
                </div>
              </div>
              <div class="calories-content">
                <p><span>Today:</span> 400</p>
                <p><span>This Week:</span> 3500</p>
                <p><span>This Month:</span> 14000</p>
              </div>
            </div>
          </div>
```

## css

```sh

/* ACTIVE CALORIES  */

.active-calories {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: rgb(214, 227, 248);
  padding: 0 10px;
  margin: 15px 10px 0;
  border-radius: 15px;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 3px;
}

.active-calories h1 {
  margin-top: 10px;
  font-size: 1.2rem;
}

.active-calories-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
}


.box {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  position: relative;
  padding: 10px 0;
  /* width: 200px; */
}

.box h2 {
  position: relative;
  text-align: center;
  font-size: 1.25rem;
  color: rgb(91, 95, 111);
  font-weight: 600;
}

.box h2 small {
  font-size: 0.8rem;
  font-weight: 600;
}


.circle {
  position: relative;
  width: 80px;
  aspect-ratio: 1/1;
  background: conic-gradient(
    from 0deg,
    #590b94 0%,
    #590b94 0% var(--i),
    #b3b2b2 var(--i),
    #b3b2b2 100%
  );
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.circle::before {
  content: "";
  position: absolute;
  inset: 10px;
  background-color: rgb(214, 227, 248);
  border-radius: 50%;
}
```

## js

```sh

```
