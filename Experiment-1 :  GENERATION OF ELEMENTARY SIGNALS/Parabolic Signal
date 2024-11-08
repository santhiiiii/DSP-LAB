% GENERATION OF PARABOLIC SIGNAL WITH DECAY
clc;
clf;

n1 = input("Enter the starting point of the signal: n_start = ");
n2 = input("Enter the ending point of the signal: n_end = ");
lambda = input("Enter the decay constant (lambda): ");

% For discrete parabolic signal
sample_points = -n1:0.1:n2;
amplitude = ((sample_points.^2) / 2) .* exp(-lambda * sample_points) .* (sample_points >= 0);  

% Subplot for discrete parabolic signal
subplot(2, 1, 1);  
stem(sample_points, amplitude, 'filled', 'LineWidth', 2);
xlabel("Sample Points");
ylabel("Amplitude");
title(sprintf("Discrete Parabolic Signal with Decay (\\lambda = %.2f)", lambda));
grid on;

% Subplot for continuous parabolic signal
subplot(2, 1, 2);  
plot(sample_points, amplitude, 'LineWidth', 2);
xlabel("Time (s)");
ylabel("Amplitude");
title(sprintf("Continuous Parabolic Signal with Decay (\\lambda = %.2f)", lambda));
grid on;
