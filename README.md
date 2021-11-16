# TinyStore

A tool help you share states between components, pages and projects, support any micro FE architecture

---

![image](https://user-images.githubusercontent.com/8454869/141887306-330e7afd-3b06-45ae-9c97-8c153e712928.png)



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
