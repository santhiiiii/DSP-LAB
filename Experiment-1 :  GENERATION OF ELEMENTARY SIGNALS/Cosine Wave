clc;
clf;

Am = input("Enter the maximum amplitude of the wave: ");
Fm = input("Enter the frequency of the wave (Hz): ");
Cy = input("Enter the number of cycles of the wave: ");

% Time vector for discrete signal
t = 0 : (1/(50 * Fm)) : Cy/Fm;  
cosine_signal = Am * cos(2 * pi * Fm * t);

% Determine max and min amplitude values
max_amplitude = max(cosine_signal);
min_amplitude = min(cosine_signal);

% Set y-axis limits
y_min = min_amplitude - 1;
y_max = max_amplitude + 1;

% Subplot for continuous cosine wave
subplot(2, 1, 1);  
plot(t, cosine_signal, 'LineWidth', 2);
hold on;
% Highlight the x-axis with a white solid line
plot(t, zeros(size(t)), 'blue-', 'LineWidth', 1.5);
title(sprintf('Continuous Cosine Wave (Frequency = %.2f Hz)', Fm));
xlabel('Time (s)');
ylabel('Amplitude');
grid on;
% Adjust y-axis limits
ylim([y_min y_max]);
hold off;  % Release the plot hold

% Subplot for discrete cosine wave
subplot(2, 1, 2);  
stem(t, cosine_signal, 'filled', 'LineWidth', 1.5);
hold on;
% Highlight the x-axis with a white solid line
plot(t, zeros(size(t)), 'blue-', 'LineWidth', 1.5);
title(sprintf('Discrete Cosine Wave (Frequency = %.2f Hz)', Fm));
xlabel('Time (s)');
ylabel('Amplitude');
grid on;
% Adjust y-axis limits
ylim([y_min y_max]);
hold off;  % Release the plot hold
