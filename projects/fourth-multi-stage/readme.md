A multi-stage Docker build is a Dockerfile technique where you use multiple FROM images in one Dockerfile
to build your app in one stage and run it in another. This lets you keep build tools out of the final image, making it smaller, faster, and more secure.

**Without multi-stage builds:**
Final image contains compilers, SDKs, build caches
Image size becomes huge
More attack surface

**->With multi-stage builds:**
Build happens in a builder image
Only required artifacts are copied to a runtime image

In this case"
Smaller image	No OS, no compiler
More secure	No shell, no attack surface
Faster	Less to pull & start
Cleaner	Build logic separated
