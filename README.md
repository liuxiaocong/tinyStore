# TinyStore

A tool help you share states between components, pages and projects, support any micro FE architecture

---

### Api

```ts
const createStore = <T extends Record<string, unknown>>(
  props: StoreType<T> = {
    nameSpace: "",
    key: "",
    crossBundle: false,
    runTime: true,
  }
): {
  useStore: () => [
    <K extends keyof T>(key: K) => T[K] | undefined,
    <K extends keyof T>(key: K, val: T[K]) => void
  ];
  get: <K extends keyof T>(key: K) => T[K] | undefined;
  set: <K extends keyof T>(key: K, val: T[K]) => void;
}
```

---

### Todo

- User ref to optimize performance
- Support default value

---

Refer to [PPT](https://docs.google.com/presentation/d/1dY7C8r6exdavVSSqMzmwfmZbeB4ahaUxnKSXfSUUpao/edit#slide=id.gec60d382a1_0_80)
