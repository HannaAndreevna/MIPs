# How to contribute

1. Review [MIP-1](https://github.com/OpenMAVN/MIPs/blob/master/MIPS/mip-1.md).
2. Fork the repository by clicking "Fork" in the top right.
3. Add your MIP to your fork of the repository. There is a [template MIP here](https://github.com/OpenMAVN/MIPs/blob/master/mip-template.md).
4. Submit a Pull Request to OpenMAVN [MIPs repository](https://github.com/OpenMAVN/MIPs).

Your first PR should be a first draft of the final MIP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new MIP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to an open GitHub issue where people can discuss the MIP as a whole.

If your MIP requires images, the image files should be included in a subdirectory of the `assets` folder for that MIP as follows: `assets/mip-N` (where **N** is to be replaced with the MIP number). When linking to an image in the MIP, use relative links such as `../assets/mip-1/image.png`.

Make sure that the 'author' line of your MIP contains either your GitHub username or your email address inside \<triangular brackets\>. If you use your email address, that address must be the one publicly shown on [your GitHub profile](https://github.com/settings/profile).

When you believe your EIP is mature and ready to progress past the draft phase, open a PR changing the state of your EIP to 'Accepted'. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the MIP - they may close the PR and request that you fix the issues in the draft before trying again.