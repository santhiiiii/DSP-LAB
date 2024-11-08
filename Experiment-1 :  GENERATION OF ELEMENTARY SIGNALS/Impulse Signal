% GENERATION OF UNIT IMPULSE SIGNAL

clc;
clf;

n1 = input("Enter the starting point of the signal: n_start = ");
n2 = input("Enter the ending point of the signal: n_end = \n");

% Declaring the axis of the signal
sample_points = -n1:1:n2;
amplitude = [zeros(1, n1) 1 zeros(1, n2)];

% Determine max and min amplitude values
max_amplitude = max(amplitude);
min_amplitude = min(amplitude);

% Set y-axis limits
y_min = min_amplitude - 0.2;
y_max = max_amplitude + 0.2;


% Subplot for discrete impulse signal
subplot(2, 1, 1);
stem(sample_points, amplitude, 'LineWidth', 2, 'MarkerSize', 4);
xlabel("Sample Points");
ylabel("Amplitude");
title("Discrete Impulse Signal");
grid on;
% Adjust y-axis limits
ylim([y_min y_max]);

% Subplot for continuous impulse signal
subplot(2, 1, 2);
plot(sample_points, amplitude, 'LineWidth', 4); 
xlabel("Sample Points");
ylabel("Amplitude");
title("Continuous Impulse Signal");
grid on;
% Adjust y-axis limits
ylim([y_min y_max]);
