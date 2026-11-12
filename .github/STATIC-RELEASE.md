# Manual static releases

After syncing upstream, open **Actions → Static release → Run workflow**.
Select the branch to build, normally `master`. Leave **tag** blank to use
the source version and commit, or enter a new tag such as
`v3.3.6-rampage.2`. Existing tags are rejected.

The workflow publishes after the four builds and their checks pass. Releases
contain Linux ARMv5TE soft-float, Linux AArch64, Linux x86_64 and Windows x64
command-line programs, along with their license notices. Linux executables use
static musl. Windows executables import only Windows system DLLs.

The build uses upstream's bundled dependency mode, including libsodium and
the reduced Mbed TLS configuration. Both libraries are required by the
current implementation.
