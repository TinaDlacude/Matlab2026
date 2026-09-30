% Question 1(a) - Bisection Method
clc; clear;

f = @(x) x^2 - x - 2;
a = 1; b = 2;
tol = 1e-4;

fa = f(a); fb = f(b);
if fa*fb > 0
    disp('No root in interval')
    return
end

iter = 0;
while (b - a)/2 > tol
    c = (a + b)/2;
    fc = f(c);

    if fc == 0
        break
    end

    if fa*fc < 0
        b = c;
        fb = fc;
    else
        a = c;
        fa = fc;
    end
    iter = iter + 1;
end

root = (a + b)/2;
fprintf('Root = %.6f\n', root);
fprintf('Iterations = %d\n', iter);
fprintf('f(root) = %.6f\n', f(root));
