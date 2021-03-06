---
id: ReaderT
title: Module ReaderT
---

[Source](https://github.com/gcanti/fp-ts/blob/master/src/ReaderT.ts)

## Functions

### ap

_function_

_since 1.0.0_

_Signature_

```ts
ap<F>(
  F: Applicative<F>
): <E, A, B>(fab: (e: E) => HKT<F, (a: A) => B>, fa: (e: E) => HKT<F, A>) => (e: E) => HKT<F, B>
```

### ask

_function_

_since 1.0.0_

_Signature_

```ts
ask<F>(F: Applicative<F>): <E>() => (e: E) => HKT<F, E>
```

### asks

_function_

_since 1.0.0_

_Signature_

```ts
asks<F>(F: Applicative<F>): <E, A>(f: (e: E) => A) => (e: E) => HKT<F, A>
```

### chain

_function_

_since 1.0.0_

_Signature_

```ts
chain<F>(
  F: Chain<F>
): <E, A, B>(f: (a: A) => (e: E) => HKT<F, B>, fa: (e: E) => HKT<F, A>) => (e: E) => HKT<F, B>
```

### fromReader

_function_

_since 1.2.0_

_Signature_

```ts
fromReader<F>(F: Applicative<F>): <E, A>(fa: Reader<E, A>) => (e: E) => HKT<F, A>
```

### getReaderT

_function_

_since 1.0.0_

_Signature_

```ts
getReaderT<M>(M: Monad<M>): ReaderT<M>
```

### map

_function_

_since 1.0.0_

_Signature_

```ts
map<F>(F: Functor<F>): <E, A, B>(f: (a: A) => B, fa: (e: E) => HKT<F, A>) => (e: E) => HKT<F, B>
```

### of

_function_

_since 1.0.0_

_Signature_

```ts
of<F>(F: Applicative<F>): <E, A>(a: A) => (e: E) => HKT<F, A>
```
