clc;
clf;

Am = input("Enter the maximum amplitude of the wave: ");
Fm = input("Enter the frequency of the wave (Hz): ");
Cy = input("Enter the number of cycles of the wave: ");

% Time vector for discrete signal
t = 0 : (1/(50*Fm)) : Cy/Fm;  
sine_wave = Am * sin(2 * pi * Fm * t);

% Determine max and min amplitude values
max_amplitude = max(sine_wave);
min_amplitude = min(sine_wave);

% Set y-axis limits
y_min = min_amplitude - 1;
y_max = max_amplitude + 1;

% Subplot for continuous sine wave
subplot(2, 1, 1);  
plot(t, sine_wave, 'LineWidth', 2);
title(sprintf('Continuous Sine Wave (Frequency = %.2f Hz)', Fm));
xlabel('Time (s)');
ylabel('Amplitude');
grid on;
% Adjust y-axis limits
ylim([y_min y_max]);

% Subplot for discrete sine wave
subplot(2, 1, 2);  
stem(t, sine_wave, 'LineWidth', 2);
title(sprintf('Discrete Sine Wave (Frequency = %.2f Hz)', Fm));
xlabel('Time (s)');
ylabel('Amplitude');
grid on;
% Adjust y-axis limits
ylim([y_min y_max]);
