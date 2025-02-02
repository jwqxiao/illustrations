import React from 'react';
import { LineChart, Line, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer } from 'recharts';

const data = [
  {
    name: 'GPT-4 (Mar 2023)',
    output_price: 60,
    input_price: 30,
  },
  {
    name: 'GPT-4 Turbo (Mar 2023)', 
    output_price: 30,
    input_price: 10,
  },
  {
    name: 'GPT-4o (2023)',
    output_price: 15,
    input_price: 5,
  },  
  {
    name: 'GPT-3.5 Turbo (Jun 2023)',
    output_price: 0.002, 
    input_price: 0.0015,
  },
  {
    name: 'GPT-4o (2024)',
    output_price: 10,
    input_price: 3,
  },
  {
    name: 'GPT-4o Mini (Jul 2024)',
    output_price: 0.6,
    input_price: 0.15,
  },
];

const toDecimal = (num) => (
  num >= 1 ? num.toFixed(2) : num.toFixed(5).replace(/0+$/, '').replace(/\.$/, '')
);

const PricingChart = () => (
  <ResponsiveContainer width="100%" height={400}>
    <LineChart data={data} margin={{ top: 20, right: 30, left: 0, bottom: 0 }}>
      <CartesianGrid strokeDasharray="3 3" />
      <XAxis dataKey="name" />
      <YAxis tickFormatter={toDecimal} />
      <Tooltip formatter={(value) => `$${toDecimal(value)}`} />
      <Legend />
      <Line type="monotone" dataKey="output_price" stroke="#8884d8" name="Output (per 1M tokens)" />
      <Line type="monotone" dataKey="input_price" stroke="#82ca9d" name="Input (per 1M tokens)" />
    </LineChart>
  </ResponsiveContainer>  
);

export default PricingChart;
