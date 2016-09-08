#Doubly Stochastic Neighbor Embedding on Spheres
DOSNES is a new method to visualize your data.

##Project Page
http://yaolubrain.github.io/dosnes/

##How to use?
Here is a simple example. Given a similartiy matrix `P`
``` 
% Normalize it to be doubly stochastic by Sinkhorn-Knopp method
for i = 1:100
    P = bsxfun(@rdivide, sum(P,1));
    P = bsxfun(@rdivide, sum(P,2));
end    

% Run t-SNE with the spherical constraint.
Y = tsne_p_sphere(P);
``` 

##Paper
[Doubly Stochastic Neighbor Embedding on Spheres] (https://github.com/yaolubrain/DOSNES) <br>
Yao Lu\*, Zhirong Yang\*, Jukka Corander <br>
(*equal contribution)
