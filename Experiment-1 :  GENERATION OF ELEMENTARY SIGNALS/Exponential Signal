% GENERATION OF EXPONENTIAL SIGNAL
clc;
clf;

% User input for signal range and exponential factor
n1 = input("Enter the starting point of the signal: n_start = ");
n2 = input("Enter the ending point of the signal: n_end = ");
lambda = input("Enter the exponential growth/decay factor: ");

% Define sample points for discrete signal
sample_points = -n1:0.05:n2;
amplitude = exp(lambda * sample_points) .* (sample_points >= 0);

% Subplot for discrete exponential signal
subplot(2, 1, 1); 
stem(sample_points, amplitude, 'filled', 'LineWidth', 2);
xlabel("Sample Points");
ylabel("Amplitude");
title(sprintf("Discrete Exponential Signal (\\lambda = %.2f)", lambda));
grid on;

% Subplot for continuous exponential signal
subplot(2, 1, 2);
plot(sample_points, amplitude, 'LineWidth', 2);
xlabel("Time (s)");
ylabel("Amplitude");
title(sprintf("Continuous Exponential Signal (\\lambda = %.2f)", lambda));
grid on;
