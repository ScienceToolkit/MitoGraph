### MitoGraph

<img src="doc/mitograph.png" width="auto" height="256" title="MoCo Logo">

MitoGraph is a fully automated image processing method and software dedicated to calculating the three-dimensional morphology of mitochondria in live cells. MitoGraph is currently optimized and validated only for quantifying the volume and topology of tubular mitochondrial networks in budding yeast [1,2]. However, MitoGraph can also be applied to mitochondria in other cell types and possibly other intracellular (or tissue) structures, with proper validation. MitoGraph is continuously being updated and we hope to be able to accurately analyze mitochondrial network topology and, eventually dynamics. Please contact us if you have questions relating to these other applications that go beyond mitochondrial volume.

[1] Matheus P Viana, Swee Lim, Susanne M Rafelski, Quantifying Mitochondrial Content in Living Cells (2015), Biophysical Methods in Cell Biology, (125) - 77-93 (http://www.sciencedirect.com/science/article/pii/S0091679X14000041)

[2] Under revision.

2018.01.08, Matheus Viana.

### How to install

Please follow the steps bellow to install MitoGraph.

1. Download the file that suits your operating system.

2. Create a new folder called MitoGraph on your Desktop.

3. Move the downloaded file to the folder you just created and rename the file to MitoGraph.

4. Open the terminal in your Mac OS (spotlight + terminal)

5. Type the following command (make sure that you are typing the space and upper cases correctly) and press return.

`cd ~/Desktop/MitoGraph`

PS: if any error message is displayed, please check the spelling of the directory that you have created.

6. Type the following command.

`chmod +xxx MitoGraph`

PS: if no error message is displayed it means that MitoGraph is ready to run.

### How to run MitoGraph

Type the following command in the terminal.

`./MitoGraph -xy 0.056 -z 0.2 -path ~/Desktop/examples`

PS: The flag -xy specifies the pixel size in microns and the flag -z specifies the z-spacing also in microns of your images. Finally, the flag -path indicates the folder that contains the images you want to analyze.

#### Optional flags

`-scales a b c` where a, b and c are numeric values specifying the initial, final and total number of scales which should be used by MitoGraph [1]. For example: `-scales 1.5 2.0 6`. Default values are a=1.0, b=1.5 and c=6.

`-thhreshold a` where a is numeric value in the range [0,1] for the post-divergence threshold. For example: `-threshold 0.1`. Default value is a=0.1667.

`-adaptive a` where a is a numeric integer value specifying that the input image should be splited into a x a blocks before the segmentation. This is useful for images withh high variablity of pixel intensity.

`-binary`: indicates that the input is a binary image. 

`-vtk`: indicates that the input data is of format VTK instead of TIFF.

### MitoGraph outputs

The output of MitoGraph will be saved in the current working directory ~/Desktop/examples. To know more about each file generated by MitoGraph, please refer to our paper [1].
