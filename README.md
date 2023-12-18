# Segment Anything inference using JavaScript

This sample web application shows how to use [Segment Anything](https://https://segment-anything.com/) neural network
to segment objects in images right in a web browser without any backend, using only JavaScript and [ONNX runtime](https://onnxruntime.ai/).

# Install

1. Clone this repository: `git clone git@github.com:AndreyGermanov/sam_onnx_javascript.git`
2. Export both encoder and decoder parts of the Segment Anything model to ONNX, using [this notebook](https://github.com/AndreyGermanov/sam_onnx_full_export/blob/main/sam_onnx_export.ipynb).
3. Copy exported `vit_b_encoder.onnx` and `vit_b_decoder.onnx` files to the root of cloned repository.

* If something went wrong with exporting, read and follow [this article](https://dev.to/andreygermanov/export-segment-anything-neural-network-to-onnx-the-missing-parts-43c8) which has a thorough explanation of this notebook.

# Run

You need to run `index.html` using any local webserver, for example internal webserver of Visual Studio Code. Ensure that
the model files `vit_b_encoder.onnx` and `vit_b_decoder.onnx` exist in the same folder with `index.html`.

Using the interface in `index.html`, upload the image, click on top left and bottom right corners of an object, that you want to segment and see extracted object without background below the image.

Also, you can export and use Vit-H or Vit-L models to ONNX using the notebook, mentioned above and then change ENCODER_MODEL_PATH and DECODER_MODEL_PATH in the `index.html`.

