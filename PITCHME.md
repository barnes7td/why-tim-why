build-lists: true

# Why Tim, Why?

## ...the big picture

---

<!-- _class: title -->

# My Caveats

- These are my opinions
- From my experience

---

<!-- _class: title -->

# The Big Questions

---

<!-- header: The Bigs -->

# Why are we using Angular?

---

<!-- header: 'The Bigs: Why are we using Angular?' -->

# Why are we using Angular?

- This conversion started with a conversion to Angular.js
- Give us the ability to upgrade Angular.js components

---

<!-- header: 'The Bigs: Why use Redux?' -->

# Why are we using ngrx (the Redux pattern)?

- State management
- Cons
  - Tons of boilerplate code need for simple actions
    - insanity of facades
  - Pushes things out into multiple files - hard to troubleshoot, hard to comprehend
  - It's a learning curve for everyone.
- Why we use a Reactive Programming patterns as much as we can.

---

# Why do we have Two separate applications running?

- What does it gain us?
  - Allowed us to manage state effectively
    - Keep things in sync
    - Update all components easily and reliably
  - Gave us built in testing

---

# What does that mean?

- We must keep 2 separate headers in sync (with different style sheets)
- What Billie and I advised as standards in Angular.js are often the exact opposite in the Angular code.
  - booleans in templates → boolean juggling

---

# Why we chose Fabric.js?

---

# Things We Do - Our opinions

---

- We save things in the store as a dictionary (not arrays)
  - But Why?
- Core/Shared concept
- Put things in modules → for lazy loading
- Why we think Presenter components are rarely useful
- Why we DO repeat ourselves inside of test files.
- We prefer shallow nesting
- We have components talk to effects and not services directly
  - Services is a catch-all term
    - Use to have things like 'plain-old \_ objects'

---

[1]

```javascript
function buildFakeOrder() {
  const fakeOrderDto = new OrderDto();
  fakeOrderDto.productGroupCode = "1";
  fakeOrderDto.productVarianceCode = "1";
  console.log("hello");
  // what is this
  fakeOrderDto.publishYear = "2019";
  fakeOrderDto.jobNumber = 37;
  return new Order(fakeOrderDto);
}
```

---

## Image Layout

### Images can be on the _left_ or the *right*â€”whichever you like.

---

# Itâ€™s **sooo** easy to change!

Try it yourself and move this image to the right

![right](logo-1.png)
