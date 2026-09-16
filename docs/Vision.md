Each of my projects originated because I had a problem I needed to solve; initially it was Codex, how do I get it to run on Android?

I started using the Codex CLI on Termux, but I had to use Danger-full-access because there was no Android backend. But at some point I wondered, there must be a solution.

I started looking around the community, but no one had built a sandbox; everyone was using danger-full-access, but that wasn't enough for me.

I have looked at many other projects, gathered inspiration, examined how they work, and experimented a lot; I have also answered my own question.

Why has no one built an Android sandbox yet?

It is extremely difficult to build a sandbox that can be enforced on all kernels; the Android system is extremely fragmented. Just because the sandbox runs on device A doesn't mean it will run the same way on device B.

To ensure that device B doesn't silently revert to danger-full-access, I built the sandbox fail-closed. If it cannot be enforced on device B, the corresponding mode will no longer function.