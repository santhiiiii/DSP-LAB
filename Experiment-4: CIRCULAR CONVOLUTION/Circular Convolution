% Circular Convolution using Matrix Method and Built-in Function

clc;
clf
close all;

% Input the sequences from the user
x = input('Enter the 1st sequence x[n] as a vector (e.g., [1, 2, 3, 4]): ');
h = input('Enter the 2nd sequence h[n] as a vector (e.g., [1, 2, 3, 4]): ');

% Length of sequences
N = max(length(x), length(h));

% Zero-pad sequences to the same length N
x = [x, zeros(1, N - length(x))];
h = [h, zeros(1, N - length(h))];

% Construct the circulant matrix for h
H = zeros(N, N);
for i = 1:N
    H(:, i) = circshift(h', i - 1); % Use column shifts to construct circulant matrix
end

% Perform the circular convolution using matrix method
y_matrix = H * x';

% Perform the circular convolution using built-in function
y_builtin = cconv(x, h, N);

% Display the results
disp('The circular convolution result using matrix method is: ');
disp(y_matrix');

disp('The circular convolution result using built-in cconv function is: ');
disp(y_builtin);

% Find the global y-limits across both results
min_y = min([y_matrix; y_builtin]) - 1;
max_y = max([y_matrix; y_builtin]) + 1;

% Plot the sequences and the circular convolution results
figure;
subplot(4, 1, 1);
stem(0:N-1, x, 'filled');
title('Input Sequence x[n]');
xlabel('n');
ylabel('x[n]');
grid on;
% Adjust y-axis limits
ylim([min(x)-1, max(x)+1]);

subplot(4, 1, 2);
stem(0:N-1, h, 'filled');
title('Input Sequence h[n]');
xlabel('n');
ylabel('h[n]');
grid on;
% Adjust y-axis limits
ylim([min(h)-1, max(h)+1]);

subplot(4, 1, 3);
stem(0:N-1, y_matrix, 'filled');
title('Circular Convolution (Matrix Method) y_{matrix}[n]');
xlabel('n');
ylabel('y_{matrix}[n]');
grid on;
% Adjust y-axis limits
ylim([min_y, max_y]);

subplot(4, 1, 4);
stem(0:N-1, y_builtin, 'filled');
title('Circular Convolution (Built-in cconv) y_{builtin}[n]');
xlabel('n');
ylabel('y_{builtin}[n]');
grid on;
% Adjust y-axis limits
ylim([min_y, max_y]);

%}
