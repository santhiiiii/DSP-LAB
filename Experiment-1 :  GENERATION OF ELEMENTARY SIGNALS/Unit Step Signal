% GENERATION OF UNIT STEP SIGNAL
clc;
clf;

n1 = input("Enter the starting point of the signal: n_start = ");
n2 = input("Enter the ending point of the signal: n_end = ");

% Discrete-time unit step signal
sample_points = -n1:0.1:n2;
amplitude = double(sample_points >= 0);

% Subplot for discrete unit step signal
subplot(2, 1, 1);  
stem(sample_points, amplitude, 'filled', 'LineWidth', 2);
xlabel("Sample Points");
ylabel("Amplitude");
title("Discrete Unit Step Signal");
grid on;
axis([-n1 n2 -0.2 1.2]);

% Subplot for continuous unit step signal
subplot(2, 1, 2);  
plot(sample_points, amplitude, 'LineWidth', 4);
xlabel("Time (s)");
ylabel("Amplitude");
title("Continuous Unit Step Signal");
grid on;
axis([-n1 n2 -0.2 1.2]);
