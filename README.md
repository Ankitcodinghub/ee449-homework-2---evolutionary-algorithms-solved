# ee449-homework-2---evolutionary-algorithms-solved
**TO GET THIS SOLUTION VISIT:** [EE449 Homework 2 – Evolutionary Algorithms Solved](https://www.ankitcodinghub.com/product/ee449-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113259&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE449 Homework 2 - Evolutionary Algorithms  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
You should prepare your homework by yourself alone and you should not share it with other students, otherwise you will be penalized.

Homework Task and Deliverables

In this homework, you will perform experiments on evolutionary algorithm and draw conclusions from the experimental results. The task is to create an image made of filled circles, visually similar to a given RGB source image (painting.png).

The implementations will be in Python language and you will be using OpenCV package to draw the images. You can install it using conda install opencv command. You can use import cv2 to use it in your code.

You should submit a single report in which your answers to the questions, the required experimental results (plots, visualizations etc.) and your deductions are presented for each part of the homework. Moreover, you should append your Python codes to the end of the report for each part to generate the results and the visualizations of the experiments. Namely, all the required tasks for a part can be performed by running the related code file. The codes should be well structured and well commented. The non-text submissions (e.g. image) or the submissions lacking comments will not be evaluated. Similarly answers/results/conclusions written in code as a comment will not be graded.

The report should be in portable document format (pdf) and named as hw2 name surname eXXXXXX where name, surname and Xs are to be replaced by your name, surname and digits of your user ID, respectively.

1 The Evolutionary Algorithm

The pseudocode for the algorithm is as follows:

Initialize population with &lt;num_inds&gt; individuals each having &lt;num_genes&gt; genes While not all generations (&lt;num_generations&gt;) are computed:

Evaluate all the individuals

Select individuals

Do crossover on some individuals

Mutate some individuals

1.1 Individuals

Each individual has one chromosome. Each gene in a chromosome represents one circle to be drawn. Each gene has at least 7 values:

• The center coordinates, (x,y)

• The radius, radius ∈Z+

• The color (red, R ∈Z, green, G ∈Z, blue, B ∈Z, alpha, A ∈R) where (R,G,B) ∈ [0,255]3 and A ∈ [0,1]

The order of the tasks to perform circle drawing is important. The circles should be drawn in the descending order of their radii. The first circle to be drawn is the one with the largest radius and the last circle to be drawn is the one with the smallest radius. The genes should be sorted accordingly.

The center does not have to be within image boundaries. However, if a circle is not within the image (it lies outside completely), the corresponding gene should be reinitialized randomly until it is.

1.2 Evaluation

In order to evaluate an individual, its corresponding image should be drawn first. Note that the chromosome order is important. The pseudocode is as follows:

Initialize &lt;image&gt; completely white with the same shape as the &lt;source_image&gt;.

For each gene in the chromosome: overlay &lt;- image Draw the circle on overlay. image &lt;- overlay x alpha + image x (1-alpha)

The fitness function, F, is

F = − X X (source imagei,j,k − imagei,j,k)2 (1)

k∈{R,G,B} 0⩽i&lt;width 0⩽j&lt;height

where source imagei,j,k is the pixel value, at ith column and jth row, in channel k in the source image. Similarly, imagei,j,k represents a pixel value in the individual’s image.

1.3 Selection

&lt;num elites&gt; number of best individuals will advance to the next generation directly. The selection of other individuals is done with tournament selection with size &lt;tm size&gt;.

1.4 Crossover

&lt;num parents&gt; number of individuals will be used for crossover. The parents are chosen among the best individuals which do not advance to the next generation directly. Two parents will create two children. Exchange of each gene is calculated individually with equal probability. The probabilities of child 1 having genei of parent 1 or parent 2 have equal probability, that is 0.5; child 2 gets the genei from the other parent which is not chosen for child 1, where 0 ⩽ i &lt; &lt;num genes&gt;.

Table 1: Parameter configurations to be experimented.

&lt;num inds&gt; 5 10 20 40 60

&lt;num genes&gt; 15 30 50 80 120

&lt;tm size&gt; 2 5 8 16

&lt;frac elites&gt; 0.04 0.2 0.35

&lt;frac parents&gt; 0.15 0.3 0.6 0.75

&lt;mutation prob&gt; 0.1 0.2 0.4 0.75

&lt;mutation type&gt; guided unguided

1.5 Mutation

There are two ways a gene can be mutated:

• Unguided

– Choose completely random values for x,y,radius,R,G,B,A.

• Guided

– Deviate the x,y,radius,R,G,B,A around their previous values.

height

– The values should be corrected to a valid one in case they are not.

2 Experimental Work

You will experiment on several different hyperparameters. Namely,

• Number of individuals (&lt;num inds&gt;)

• Number of genes (&lt;num genes&gt;)

• Tournament size (&lt;tm size&gt;)

• Number of individuals advancing without change (&lt;num elites&gt;)

• Number of parents to be used in crossover (&lt;num parents&gt;)

• Mutation probability (&lt;mutation prob&gt;)

• Mutation type (guided or unguided)

To see the effect of each hyperparameter, run the algorithm for each value in a row given in Table 1 while using default values for the other hyperparemeters. The default values are bolded. Use &lt; num generations &gt;= 10000.

For each hyperparameter, explain its effect and give the value which produces the best result. For each experiment, you need to include:

• fitness plot from generation 1 to generation 10000

• fitness plot from generation 1000 to generation 10000

• the corresponding image of the best individual in the population at every 1000th generation.

3 Discussion

4 Remarks

1. Because of the nature of assignment in Python, be careful how you use them. Consider the following:

a = [[1, 2], [3, 4]] b = [a[0], a[0]] b[0].append(5) print(b) # prints [[1, 2, 5], [1, 2, 5]] print(a) # prints [[1, 2, 5], [3, 4]]

2. You can use cv2.circle to draw circles and cv2.addWeighted to blend images.

3. Because the underlying type for the image is np.uint8, be careful of possible overflows.

4. You are advised to use classes to implement genes, individuals and populations. It will make debugging easier.
