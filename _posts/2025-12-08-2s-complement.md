---
layout: post
title: 2's Complement Derivation
date: 2025-12-08
categories: cs, binary, bits, negative numbers, derivation, proof, math, 2's complement
permalink: /2s-complement
---

If you have ever taken CS in high school or college, you have probably been taught about how to represent negative numbers in binary using 2's complement.

But teachers generally just tell you to "flip the bits and add one" without really explaining why it works---similar to how high school teachers treat math formulas.

I have never liked memorising without understanding when it comes to learning, so I came up with an intuitive derivation and wrote this blog post to share it in hopes that somebody may find it useful.

## How Does 2's Complement Work?

Say there is a number `x` represented by `n` binary digits (bits).
Since each bit can be `0` or `1`, there are 2^n possible combinations for the string of bits that represent values ranging from zero to 2^n - 1, and thus `x` is always less than 2^n.

If we flip all the bits of `x` using the bitwise NOT operator (`~`), we get a new number with `1` bits where there were `0`'s in `x` and `0` bits where there were `1`'s in `x`.
We will call this new number `~x`, where `x + ~x = 2^n - 1`, since 2^n - 1 has all `n` number of bits set to `1`.

Rearranging the above equation for `x`, we get `x = (2^n - 1) - ~x`.
It is then easy to find that

`-x = -(2^n - 1 - ~x) = -2^n + 1 + ~x`.

Now start to see the picture of where "flip the bits and add one" comes from.

But we cannot just flip bits and add 1 to get `-x` with ordinary bits, that would just be `~x + 1`.
We are still missing the `-2^n` in the equation, but how would we get that?

Currently, since the value of the most significant bit is `2^(n-1)`, if we add another bit from the left, its place value would be `2^(n-1) * 2 = 2^n`.
Now all we have to do is define the value of that new bit to be negative to get `-2^n`.
When we flip the bits of `x`, this new bit we added will also get flipped along with it.

## Conclusion

Putting all the pieces together, we get that for a number `x` represented by `n` bits (with an extra bit having a place value of `-2^n`) where `x = (2^n - 1) - ~x`, you would need to flip its bits and add one to get `-2^n + ~x + 1 = -x`.

Hopefully after reading this, you will have gained a better understanding of using 2's complement for converting binary numbers to negative.

<script src="https://giscus.app/client.js"
        data-repo="de-soot/de-soot.github.io"
        data-repo-id="R_kgDOK6_5tA"
        data-category="Announcements"
        data-category-id="DIC_kwDOK6_5tM4CflCT"
        data-mapping="title"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="preferred_color_scheme"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>
